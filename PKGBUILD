# Maintainer: Doug Douglass <douglass.doug@gmail.com>
# Originator: Kyle Keen <keenerd@gmail.com>
pkgname=pacmatic
pkgver=20240220
pkgrel=1
pkgdesc="A pacman wrapper to avoid bricking your system and such other surprises."
arch=('any')
url="https://github.com/douglassd/pacmatic"
#original: url="http://kmkeen.com/pacmatic/"
license=('GPL')
depends=('pacman' 'bash' 'expac')
makedepends=()
optdepends=('vim: for vimdiff'
            'html2text: for prettier news'
            'fakeroot: for cron-pacmatic script')
source=("cron-pacmatic"
        "_pacmatic"
        "pacmatic"
        "pacmatic.1")
md5sums=('6abab9b8bf9ba406bbdf21cc1b8798eb'
         '1c369c8fe595cbb41d04e214efd39a1e'
         'd3f080d325fa8fc4b00265224142b441'
         '9a65117de99600fd6e92cbbdd10395c5')

package() {
  cd "$srcdir"
  install -Dm0755 pacmatic      "$pkgdir/usr/bin/pacmatic"
  install -Dm0755 cron-pacmatic "$pkgdir/usr/bin/cron-pacmatic"
  install -Dm0644 pacmatic.1    "$pkgdir/usr/share/man/man1/pacmatic.1"
  install -Dm0644 ../_pacmatic  "$pkgdir/usr/share/zsh/site-functions/_pacmatic"
}

