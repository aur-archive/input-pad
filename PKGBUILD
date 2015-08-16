# Maintainer: Limao Luo <luolimao+AUR@gmail.com>

pkgname=input-pad
pkgver=1.0.2
pkgrel=1
pkgdesc="Graphical tool to input special characters into text-based applications"
arch=(i686 x86_64)
url=http://input-pad.googlecode.com
license=(LGPL2.1)
depends=(gtk2 libxklavier)
makedepends=(python2 swig)
options=(!libtool)
source=($url/files/$pkgname-$pkgver.tar.gz)
sha256sums=('572179455727b3b45238ccf4eaa5a2ddac5fff0404b8719d4258d63698498799')
sha512sums=('e8330e370f9018d4998cef0a6df5503373fedbcb5c6b04989448a8ea010b7d0f1b785a845530d5cde29dfe61ea5d2ee9bdb3e30ebf1eedfa8a206271e36b8571')

build() {
    cd $pkgname-$pkgver/
    ./configure --prefix=/usr --enable-nls
    make
}

package() {
    make -C $pkgname-$pkgver DESTDIR="$pkgdir" install
}
