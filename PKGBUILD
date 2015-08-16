# Maintainer BlackIkeEagle < ike DOT devolder AT gmail DOT com >

pkgname=kmtail
pkgver=0.9.1
pkgrel=3
pkgdesc="KDE tail tool"
arch=('i686' 'x86_64')
url="http://kde-apps.org/content/show.php/KmTail?content=124134"
license=('GPL')
depends=('kdebase-workspace' 'turbotail')
makedepends=('cmake' 'automoc4' 'docbook-xsl')
source=("http://www.binro.org/$pkgname-$pkgver.tar.bz2")
sha256sums=('abf8a10139e08e3aa923865cc665ff5b55e05e901116bfc0579c6dc45d571851')

build() {
	cd "$pkgname-$pkgver"

	[ -e build ] && rm -rf build
	mkdir build && cd build
	cmake -DCMAKE_INSTALL_PREFIX=/usr ..
	make
}

package() {
	cd "$pkgname-$pkgver/build"
	make DESTDIR="$pkgdir" install
}
