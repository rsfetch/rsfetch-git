# Maintainer: Kied Llaentenn <@kiedtl>
# Maintainer: ValleyKnight <valleyknight@protonmail.com>

pkgname=rsfetch-git
pkgver=1.4.0
pkgrel=1
pkgdesc="Fast (0.01s - 0.2s execution time) and somewhat(?) minimal fetch program written in Rust."
url="https://github.com/phate6660/rsfetch"
license=('Unlicense')
depends=()
conflicts=('rsfetch-bin')
makedepends=("rust")
arch=("i686" "x86_64")
source=("rsfetch-git::git+https://github.com/phate6660/rsfetch#branch=master")

build() {
	cd "${srcdir}/${pkgname}"
	make build
}

package() {
	mkdir -p ${pkgdir}/usr/bin
	mkdir -p ${pkgdir}/usr/share/licenses/${pkgname}

	install -Dm 755 ${srcdir}/${pkgname}/target/release/fetch ${pkgdir}/usr/bin/rsfetch
	install -Dm 644 ${srcdir}/${pkgname}/LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

sha512sums=('SKIP')