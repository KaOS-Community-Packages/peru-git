pkgname=peru-git
pkgrel=1
pkgdesc='A tool for fetching code'
arch=('x86_64')
url='https://github.com/buildinspace/peru'
license=('MIT')
pkgver=478.219ea27
pkgver() {
  cd "$srcdir/peru"
  echo $(git rev-list --count master).$(git rev-parse --short master)
}
depends=('git' 'python3')
makedepends=('python3-setuptools')
optdepends=(
  'mercurial: fetching from hg repos'
  'subversion: fetching from svn repos'
)
source=('git://github.com/buildinspace/peru')
sha512sums=('SKIP')

package() {
  cd "$srcdir/peru"
  python3 setup.py install --root="$pkgdir"
}
