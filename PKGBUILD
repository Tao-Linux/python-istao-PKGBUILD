# Maintainer: Nekosis <37462865+Nekosis@users.noreply.github.com>
pkgname='python-istao'
_name=${pkgname#python-}
pkgver=0.4
pkgrel=1
pkgdesc="Library for Tao Python applications to check if the intended operating system is being used"
arch=('any')
url="https://github.com/Tao-Linux/python-istao"
license=('GPL')
depends=('python' 'python-distro' 'python-colorama')
makedepends=('python-setuptools')
source=("https://files.pythonhosted.org/packages/source/${_name::1}/$_name/$_name-$pkgver.tar.gz")
sha256sums=('64356078e30bb63caf9c8912c9f0c72e29de943246966f4d561b8400eaef9292')

build() {
    cd "$_name-$pkgver"
    python setup.py build
}

package() {
    cd "$_name-$pkgver"
    python setup.py install --root="$pkgdir" --optimize=1
}
