# Maintainer: Sakuraba Amane <tobiichiamane@archlinuxcn.org>

pkgname=nvchecker2yaml
pkgver=1
pkgrel=1
pkgdesc="Help Arch CN maintainers switch from nvchecker to lilac.yaml"
arch=('any')
url="https://github.com/TobiichiAmane/nvchecker2yaml"
license=('GPLv3')
makedepends=('git')
source=('git://github.com/TobiichiAmane/nvchecker2yaml.git')
md5sums=('SKIP')
depends=('git' 'bat')

pkgver() {
	cd "nvchecker2yaml" || exit 1
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

check() {
	cd "$srcdir/nvchecker2yaml" || exit 1
}

package() {
	cd "nvchecker2yaml" || exit 1
	install -Dm755 "$srcdir/nvchecker2yaml/src/n2y" "$pkgdir/usr/bin/n2y"
	install -Dm644 "$srcdir/nvchecker2yaml/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
