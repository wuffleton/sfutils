# $Id$
# Maintainer: wuffleton <woof@null.dog>
# Contributor: Felix Golatofski <contact@xdfr.de>
# Contributor: Ido Rosen <ido@kernel.org>

pkgname='sfutils'
pkgdesc="Solarflare Utilities for Linux (sfupdate, sfboot, sfctool, etc.)"
pkgver='8.2.2.1001'
pkgrel=1
arch=('x86_64')
url='https://support-nic.xilinx.com/wp/drivers'
license=('custom')
makedepends=('rpmextract')
options=('!libtool' '!strip' '!makeflags' '!buildflags' 'staticlibs')
source=(SF-107601-LS-71_Solarflare_Linux_Utilities_RPM_\(64bit\).zip::"https://support-nic.xilinx.com/wp/drivers?sd=SF-107601-LS-71&pe=1945")
sha512sums=('2484bc3614c997623b6bd837a8397540afb0192b2656a57e35789dcdcd73665084e09b6fceeb5f1399da334ba868239262ce6928da643427ab44fa6ae05c0b16')

prepare() {
  rpmextract.sh ${srcdir}/${pkgname}-${pkgver}-${pkgrel}.x86_64.rpm
}

package() {
  cd "${srcdir}"
  mv "${srcdir}/usr" "${pkgdir}/."
  mv "${pkgdir}/usr/sbin" "${pkgdir}/usr/bin"
}
