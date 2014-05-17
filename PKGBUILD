# Author: Christoph Gysin <christoph.gysin@gmail.com>

_realpkgname="keystone"
pkgname="openstack-${_realpkgname}-dev"
pkgdesc="OpenStack keystone development dependencies"
pkgver=1
pkgrel=1
arch=('any')
license=('custom')
url="https://github.com/openstack/${_realpkgname}"
depends=(
    'openstack-keystone-git'
    'git'
    'flake8-python2'
    'python2-extras'
    'python2-mimeparse'
    'python2-pbr'
    'python2-subunit'
    'python2-testtools'
    'python2-virtualenv'
)
install="${pkgname}.install"
source=(${pkgname}.install
        openstack-keystone-python2.patch)
md5sums=('0557a63655205b7066d4eab468704e8b'
         'd1450bb8f774f1a0aa489e451e23d17f')

package() {
    install -D $srcdir/openstack-keystone-python2.patch \
        $pkgdir/usr/share/$pkgname/python2.patch
}
