# Contributor: Bartek Iwaniec <hash87 [at] gmail [dot] com>

pkgname=fsrunner
pkgver=0.7.5
pkgrel=2
pkgdesc="FSRunner is a kde runner, the idea is to give you instant access to any file or directory you need."
arch=('i686' 'x86_64')
url="http://www.kde-look.org/content/show.php/fsrunner+for+KRunner?content=100057"
license=('GPL')
depends=('kdebase-workspace>=4.9')
makedepends=('cmake' 'automoc4')
source=(http://fsrunner.googlecode.com/files/${pkgname}-${pkgver}.tgz)
md5sums=('a5bbc802ae94a23b91e1851e44a0558b')

build() {

  cd ${srcdir}/${pkgname}-${pkgver}
  cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` -DCMAKE_BUILD_TYPE=Release
  make || return 1
  make DESTDIR=${pkgdir} install || return 1

}

