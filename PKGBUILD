# Maintainer: Sebastien Luttringer <seblu+arch@seblu.net>

pkgname=perf
pkgver=3.1.2
pkgrel=1
pkgdesc="Linux kernel $pkgver performance tool"
license=('GPL2')
arch=('i686' 'x86_64')
url='http://www.kernel.org'
options=(!strip)
depends=('python2' 'perl' 'libnewt' 'elfutils')
makedepends=('asciidoc' 'xmlto')
source=("http://ftp.kernel.org/pub/linux/kernel/v3.0/linux-$pkgver.tar.xz") 
md5sums=('24027361d3ea6ea2cdd7bbdd2effe43f')

build() {
  cd linux-$pkgver/tools/perf
  make PYTHON=python2 DESTDIR="${pkgdir}/usr" all man
}

package() {
  cd linux-${pkgver}/tools/perf
  make PYTHON=python2 DESTDIR="${pkgdir}/usr" install install-man
}
# vim:set ts=2 sw=2 ft=sh et:
