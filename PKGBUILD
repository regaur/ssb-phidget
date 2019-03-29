# Maintainer: Jan Boelsche <jan@lagomorph.de>
pkgname=ssb-phidget
pkgver=1.0.0
pkgrel=1
pkgdesc="Scuttlebot plugin for phidget I/O boards"
arch=('any')
url=""
license=('MIT')
groups=()
depends=(
  'nodejs'
  'libphidget22'
  'libphidget22extra'
  'phidget22networkserver'
)
makedepends=('npm')
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
source=()

pkgver () {
  npm view ${pkgname}@latest version
}

package () {
  source "$HOME/.nvm/nvm.sh"
  nvm use 10.8.0
  local _npmdir="${pkgdir}/usr/lib/node_modules/"
  mkdir -p $_npmdir
  npm install -g --prefix "${pkgdir}/usr" ${pkgname}@${pkgver}
}
