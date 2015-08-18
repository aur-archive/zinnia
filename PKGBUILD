# Maintainer: Humbert Julien <julroy67 [AT] gmail.com>

pkgname=zinnia
pkgver=0.06
pkgrel=1
pkgdesc="Simple, customizable and portable online hand recognition system based on Support Vector Machines"
arch=('i686' 'x86_64')
url="http://zinnia.sourceforge.net/"
license=('BSD')
depends=('gcc-libs')
makedepends=('libtool')
source=("http://downloads.sourceforge.net/project/$pkgname/$pkgname/$pkgver/$pkgname-$pkgver.tar.gz")
sha256sums=('ece3af93f937282971634fd81d3e997f848e8cfa958220e26a4564ca064ac20b')

build() {
	cd "$srcdir/$pkgname-$pkgver"
	
	./configure --prefix=/usr
	make || return 1
	make DESTDIR=$pkgdir install || return 1
	
	install -D -m644 $srcdir/$pkgname-$pkgver/COPYING $pkgdir/usr/share/licenses/$pkgname/LICENSE
}
