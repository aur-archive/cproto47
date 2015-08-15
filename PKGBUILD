# Maintainer: Vivien Maisonneuve <v dot maisonneuve at gmail dot com>
# Category: devel
pkgname='cproto47'
pkgver='4.7l'
pkgrel=3
pkgdesc='Generates function prototypes from C source'
arch=('i686' 'x86_64')
url='http://invisible-island.net/cproto/cproto.html'
license=('custom: public domain')
provides=('cproto'=$pkgver)
conflicts=('cproto')
source=("ftp://invisible-island.net/cproto/cproto-$pkgver.tgz")
md5sums=('ccf6aa22afd35eb5f0185b0d32030293')

build() {
    cd "$srcdir/cproto-$pkgver"
    ./configure --prefix=/usr
    make
}

check() {
    cd "$srcdir/cproto-$pkgver"
    make check
}

package() {
    cd "$srcdir/cproto-$pkgver"
    make prefix="$pkgdir"/usr install
}
