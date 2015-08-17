# Maintainer: Storm Dragon <stormdragon2976@gmail.com> 

_pkgname=pypump
pkgname=pypump2-git
pkgver=v0.5.r76.gc73e093
pkgrel=1
pkgdesc="An interface to the pump.io API's."
arch=('any')
url="https://github.com/xray7224/$_pkgname"
license=('GPL3')
depends=('python2')
makedepends=('python2-setuptools')
source=("$_pkgname::git+git://github.com/xray7224/$_pkgname.git")
md5sums=('SKIP')

pkgver() {
  cd "${srcdir}/$_pkgname"
  git describe --long --tags | sed -r 's/([^-]*-g)/r\1/;s/-/./g'
}
 
package() {
  cd "${srcdir}/$_pkgname"
  python2 setup.py install --root="${pkgdir}/" --optimize=1
}
