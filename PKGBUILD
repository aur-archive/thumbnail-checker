# Contributor: Raphael Scholer <arch_rscholer@gmx.de>
# Maintainer: JB26 <jb007xy@gmail.com>
pkgname=thumbnail-checker
pkgver=0.1
pkgrel=9
pkgdesc="Thumbnail's wasted space estimator."
arch=('i686' 'x86_64')
url='http://blogs.gnome.org/gpoo/2006/08/30/'
license=('unknown')
depends=('gnome-vfs' 'gnome-python')
makedepends=('patch')
source=('http://www.gnome.org/~gpoo/bag/thumbnail-checker/thumbnail-checker.py' \
	'http://www.gnome.org/~gpoo/bag/thumbnail-checker/thumbnail-checker.glade' \
	'thumbnail-checker.patch' \
	'thumbnail-checker')
md5sums=('a33e74985f7f032105a32662ea99ed8c' \
	'c0eac2415983237796bcf5848237a400' \
	'ec7e35ab7a65875322c529d502d8d071' \
	'6f8ad28878afbbdb1244332536312c91')
build () {
	cd $startdir
	patch < ./thumbnail-checker.patch || return 1
	install --verbose -m 755 -D thumbnail-checker "$startdir/pkg/usr/bin/thumbnail-checker"
	install --verbose -m 744 -D thumbnail-checker.py "$startdir/pkg/usr/share/thumbnail-checker/thumbnail-checker.py"
	install --verbose -m 744 -D thumbnail-checker.glade "$startdir/pkg/usr/share/thumbnail-checker/thumbnail-checker.glade"
}
