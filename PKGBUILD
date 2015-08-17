# Maintainer: Lukas Jirkovsky <l.jirkovsky@gmail.com>
pkgname=ocl-icd
pkgver=2.2.3
_pkgver=598
pkgrel=1
pkgdesc="OpenCL ICD Bindings"
arch=('i686' 'x86_64')
url="https://forge.imag.fr/projects/ocl-icd/"
license=('GPL')
depends=('glibc')
makedepends=('ruby' 'opencl-headers12')
checkdepends=()
provides=('libcl')
conflicts=('libcl')
source=(http://forge.imag.fr/frs/download.php/$_pkgver/$pkgname-$pkgver.tar.gz)
md5sums=('6b4733e72c67bb28f4e27272ced6fb3d')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}

check() {
  cd "$srcdir/$pkgname-$pkgver"
  make -k check
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
