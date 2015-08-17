# Maintainer: Massimiliano Torromeo <massimiliano.torromeo@gmail.com>
# Contributor: Si Feng <sci.feng at gmail.com>
# Contributor: LeeF <leef at hushmail.com>
# Contributor: Jim Weirch <jim.weirich at gmail.com>

pkgname=ruby-enterprise-rake
pkgver=0.9.2.2
pkgrel=3
pkgdesc="A Make-like program implemented in Ruby"
arch=('any')
url="http://rubygems.org/gems/rake"
license=('MIT')
depends=('ruby-enterprise')
source=(http://rubygems.org/gems/rake-$pkgver.gem)
noextract=(rake-$pkgver.gem)

build() {
	cd "$srcdir"
	local _gemdir=`/opt/ruby-enterprise/bin/ruby -rubygems -e'puts Gem.default_dir'`
	/opt/ruby-enterprise/bin/gem install --no-user-install --ignore-dependencies -i "$pkgdir$_gemdir" rake-$pkgver.gem
	install -dm0755 "$pkgdir/usr/share/licenses/$pkgname"
	ln -s "$_gemdir/gems/rake-$pkgver/MIT-LICENSE" "$pkgdir/usr/share/licenses/$pkgname/"
	mv "$pkgdir$_gemdir/bin" "$pkgdir/opt/ruby-enterprise/bin"
}

md5sums=('28e731d5c59dd721d6387f80b25a2ba1')
