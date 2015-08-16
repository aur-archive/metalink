# Maintainer: Limao Luo <luolimao+AUR@gmail.com>
# Contributor: Sausageandeggs <sausageandeggs@archlinux.us>

pkgname=metalink
pkgver=0.3.6
pkgrel=2
pkgdesc="Commandline metalink generator"
arch=(i686 x86_64)
url=http://sourceforge.net/projects/metalinks/
license=(GPL2)
depends=(libgcrypt boost-libs)
source=(http://sourceforge.net/projects/metalinks/files/Metalink%20commandline/$pkgver/$pkgname-$pkgver.tar.gz)
sha256sums=('c4dc2a995b82d4abe23856d28687a5b5e10b9b391acd8e247bd3791e63ae7e9a')
sha512sums=('d958fe235d21cf052945a98a03d8ce569fffa45a3451426bab7afce74ef909e8f9712a78883dd9bd31b78d3cbccd283bb0ec881557ab707723a6026ae7ff861e')

build() {
    cd $pkgname-$pkgver/
    ./configure --prefix=/usr
    make
}

package() {
    make -C $pkgname-$pkgver DESTDIR="$pkgdir" install
}
