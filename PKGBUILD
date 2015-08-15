# Contributor : Yanganto <yanganto@gmail.com>
# Contributor : Daniel YC Lin <dlin.tw at gmail>
# Maintainer : Louie Chen <louie23 at gmail>

pkgname=betaradio
pkgver=1.6
pkgrel=4
arch=('i686' 'x86_64' )
license=('GPL3')
pkgdesc="An easy way to listen to internet radio of Taiwan."
url="http://code.google.com/p/betaradio/"
depends=('gtk3' 'json-glib' 'libsoup' 'libltdl' 'gstreamer' 'gst-plugins-good' 'gst-plugins-bad' 'gst-plugins-ugly' 'gst-libav' 'openal')
makedepends=('vala' )
conflicts=('betaradio-git')
source=(https://github.com/fourdollars/betaradio/releases/download/$pkgver/$pkgname-$pkgver.tar.xz
        betaradio.install)
md5sums=('8e50b341cc65d0c6a22c96d835d109c5'
         '45ab05125b7409da2768c18182818bb0')
install=betaradio.install
options=()

build() {
    cd "$srcdir/$pkgname-$pkgver"
    ./configure --prefix=/usr
    make
}

package() {
    cd "$srcdir/$pkgname-$pkgver"
    make DESTDIR="$pkgdir" install
}
# vim:et sw=4 ts=4 ai
