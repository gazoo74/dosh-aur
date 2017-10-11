# Maintainer: Gaël PORTAY <gael.portay@savoirfairelinux.com>

pkgname=dosh
pkgver=1.0.1
pkgrel=2
pkgdesc='Docker shell'
arch=('any')
url="https://github.com/gazoo74/$pkgname"
license=('MIT')
depends=('docker')
makedepends=('asciidoctor')
source=("https://github.com/gazoo74/$pkgname/archive/$pkgver.tar.gz")
md5sums=('dd7952566643a7e7176d91864db1e001')

build() {
	cd "$srcdir/$pkgname-$pkgver"

	make doc
}

package() {
	cd "$srcdir/$pkgname-$pkgver"

	install -d "$pkgdir/usr/bin/"
	install -m 755 dosh "$pkgdir/usr/bin/"
	install -d "$pkgdir/usr/share/man/man1/"
	install -m 644 dosh.1.gz "$pkgdir/usr/share/man/man1/"
	install -d "$pkgdir/usr/share/bash-completion/completions"
	install -m 644 bash-completion "$pkgdir/usr/share/bash-completion/completions/dosh"
}
