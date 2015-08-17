# Maintainer: James Bulmer <nekinie@gmail.com>

pkgname="python2-ceilometerclient-deb"
pkgver=1.0.8
pkgrel=2
pkgdesc="Client library for Openstack"
arch=("i686" "x86_64")
url="http://docs.openstack.org/developer/python-ceilometerclient/"
license=("Apache")

depends=(
  "python2"
  "python2-pbr"
  "python2-httplib2"
  "python2-iso8601"
  "python2-prettytable"
  "python2-keystoneclient-deb"
  "python2-six"
)

makedepends=("python2-setuptools")
conflicts=("python2-ceilometerclient" "python2-ceilometerclient-git")
source=("http://archive.ubuntu.com/ubuntu/pool/main/p/python-ceilometerclient/python-ceilometerclient_${pkgver}.orig.tar.gz")
md5sums=("028c21693ce250ceef99e9cebcc9d476")

build() {
  cd "${srcdir}/python-ceilometerclient-${pkgver}/"
  python2 setup.py build
}

package() {
  cd "${srcdir}/python-ceilometerclient-${pkgver}/"
  python2 setup.py install --root="${pkgdir}/" --optimize=1
}