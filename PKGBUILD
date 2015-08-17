# Maintainer: xzy3186 <xzy3186(at)gmail>
# Contributors: Bob Fanger <bfanger(at)gmail>, Filip <fila pruda com>, Det <nimetonmaili(at)gmail>
# Based on [community-testing]'s r8168: https://projects.archlinux.org/svntogit/community.git/tree/trunk?h=packages/r8168

pkgname=r8168-dkms
_basename=r8168
pkgver=8.039.00
pkgrel=4
pkgdesc="A kernel module for Realtek 8168 network cards with dkms support"
url="http://www.realtek.com.tw"
license=("GPL")
arch=('i686' 'x86_64')
depends=('glibc' 'dkms')
conflicts=('r8168' 'r8168-ck' 'r8168-pf' 'r8168-all' 'r8168-lts' 'r8168-zen' 'r8168-openvz' 'r8168-openvz-testing')
#makedepends=('linux-headers')
#source=("https://r8168.googlecode.com/files/$_basename-$pkgver.tar.bz2"
source=("http://r8168dl.appspot.com/files/r8168-${pkgver}.tar.bz2"
        "dkms.conf" "linux40.patch")
install=$_basename.install
sha256sums=('767d922270274e781d8d42493a0021db1cafcb0388ac62564d0c0c3d82703edd'
'341d7b6358ec5b3309fde4d01f1313b4e7c001e012572decf3924593c58fc77f'
'e6087439b30c8f6c26113c182dd1f95044d918241b1c281b6e84b9a334e68910')

package() {
   cd $srcdir/$_basename-$pkgver
   mkdir -p $pkgdir/usr/src/$pkgname-$pkgver/patches
   cp -pr * $pkgdir/usr/src/$pkgname-$pkgver
   cp $srcdir/dkms.conf $pkgdir/usr/src/$pkgname-$pkgver
   cp $srcdir/linux40.patch $pkgdir/usr/src/$pkgname-$pkgver/patches/
}
