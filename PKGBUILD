pkgname=st-no-alpha
gitname=st-no-alpha
pkgver=0.8.2
pkgrel=1
pkgdesc='Dynamic Window Manager for X'
arch=('x86_64')
source=('git+https://github.com/SearyBlue/st-no-alpha')
sha1sums=('SKIP')
provides=('st-no-alpha')
conflicts=('st' 'st-git')

build() 
{
	cd "$srcdir/$gitname"
	cat /home/kirito/.config/st-no-alpha/config.h > config.h
	make
}

package() 
{
  	cd "$srcdir/$gitname"
  	make PREFIX=/usr DESTDIR="${pkgdir}" install
}
