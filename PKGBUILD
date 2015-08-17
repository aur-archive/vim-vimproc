pkgname=vim-vimproc
pkgver=8.0
pkgrel=1
pkgdesc="Interactive command execution in vim"
arch=('i686' 'x86_64')
url="https://github.com/Shougo/vimproc.vim"
license=('MIT')
depends=('vim>=7.0')
provides='vim-vimproc'
conflicts='vim-vimproc-git'
groups=('vim-plugins')
install=vimdoc.install
source=("$pkgname-$pkgver.tar.gz"::"https://github.com/Shougo/vimproc.vim/archive/ver.$pkgver.tar.gz")
sha1sums=('9b27db82efd641ed7726167e4aa028a64f17598f')

build() {
	cd "$srcdir/vimproc.vim-ver.$pkgver"
	make -f make_unix.mak
}

package() {
	cd "$srcdir/vimproc.vim-ver.$pkgver"
	installpath="$pkgdir/usr/share/vim/vimfiles"

	install -d "$installpath"/autoload/vimproc
	install -Dm644 autoload/vimproc.vim "$installpath"/autoload/vimproc.vim
	install -Dm644 autoload/vimproc_*.so "$installpath"/autoload/
	install -Dm644 autoload/vimproc/*.vim "$installpath"/autoload/vimproc/
	install -Dm644 doc/vimproc.txt "$installpath"/doc/vimproc.txt
	install -Dm644 plugin/vimproc.vim "$installpath"/plugin/vimproc.vim
}
