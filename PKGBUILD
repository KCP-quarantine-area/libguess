pkgname=libguess
pkgver=1.2
pkgrel=1
pkgdesc='High-speed character set detection library'
url='http://atheme.org/projects/libguess.html'
license=('custom')
arch=('x86_64')
source=("http://rabbit.dereferenced.org/~nenolod/distfiles/libguess-${pkgver}.tar.bz2")
sha1sums=('1fb51ac3f8f8f1ee8fd29474354bd04d1130b52d')

build() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	./configure --prefix=/usr
	make
}

package() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	make DESTDIR="${pkgdir}" install
	install -D COPYING "${pkgdir}"/usr/share/licenses/libguess/COPYING
}
