# Maintainer: Kannan Thambiah <pygospa at gmail dot com>

pkgname=mopidy-listenbrainz
pkgver=2.0.1
pkgrel=1
pkgdesc="Mopidy extension for scrobbling played tracks to listenbrainz"
arch=("any")
url="https://github.com/suaviloquence/mopidy-listenbrainz"
license=("Apache-2.0")
depends=(
	"mopidy"
	"python"
	"python-pykka"
	"python-pylast"
	"python-setuptools"
)
makedepends=(
	"python-build"
	"python-installer"
	"python-wheel"
)

source=("$pkgname-$pkgver.tar.gz::$url/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('780102752f4327fff81dc7c27f40cd7688e7bfd355463be444dd9c2ae3981e09')

build() {
	cd "$pkgname-$pkgver"
	python -m build --wheel --no-isolation
}

package() {
	cd "$pkgname-$pkgver"
	python -m installer --destdir="$pkgdir" dist/*.whl
}
