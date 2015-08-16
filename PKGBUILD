# Maintainer: Zatherz <zatherz[at]linux[dot]com>
pkgname=liborbos-text-git
pkgver=r0.g547ed88
pkgrel=1
pkgdesc="Library containing text routines for the Orb OS programs (and not only)."
url="http://orbos.github.io/"
arch=('x86_64' 'i686')
license=('GPLv2')
depends=()
makedepends=('git' 'make')
source=("git://github.com/Zatherz/liborbos")
md5sums=("SKIP")

pkgver() {
  cd "liborbos"
  git describe --long --all | sed -r 's/([^-]*-g)/r\1/;s/-/./g;s/heads\/master.//g'
}

build() {
  cd "$srcdir/liborbos/liborbos-text"
  make
}

package() {
  cd "$srcdir/liborbos/liborbos-text"
  make DESTDIR="$pkgdir" install
}
