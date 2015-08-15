# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Mauro Andreolini <mauro.andreolini@unimore.it>
pkgname=goofile
pkgver=1.5
pkgrel=1
epoch=
pkgdesc="Search specific file types in a given domain"
arch=('any')
url="http://code.google.com/p/goofile/"
license=('custom')
groups=()
depends=(python2)
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("http://goofile.googlecode.com/files/goofilev1.5.zip"
  "LICENSE"
)
noextract=()
md5sums=('a32a5884501d289e633fe9103d6046da'
  '9583d27c8aa1fc328fa6a8e747c88940'
)

build() {
  cd "${srcdir}/${pkgname}v${pkgver}"
  sed -i -e "s|env python|env python2|" goofile.py
}

package() {

  install -D -m 644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"

  cd "${srcdir}/${pkgname}v${pkgver}"
  install -D -m 755 goofile.py "${pkgdir}/usr/bin/goofile.py"
}

# vim:set ts=2 sw=2 et:
