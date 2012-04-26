 # Contributor: Max Gonzih <iam AT gonzih DOT org>
 pkgname=shelr
 pkgver=0.15.1
 pkgrel=1
 pkgdesc="Shelr.tv client"
 arch=(any)
 url="http://shelr.tv"
 license=(GPLv3)
 depends=(ruby ruby-json)
 makedepends=(rubygems)
 source=(http://rubygems.org/downloads/shelr-$pkgver.gem)
 noextract=(shelr-$pkgver.gem)
 md5sums=(1e423653ceee7c285f932f513593ad3b)

 build() {
   cd $srcdir

   if which rvm &> /dev/null; then
     local _gemdir="$(rvm system do ruby -rubygems -e'puts Gem.default_dir')"
     rvm system do gem install --no-user-install --ignore-dependencies --verbose -i "$pkgdir$_gemdir" -n "$pkgdir"/usr/bin shelr-$pkgver.gem
   else
     local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
     gem install --no-user-install --ignore-dependencies --verbose -i "$pkgdir$_gemdir" -n "$pkgdir"/usr/bin shelr-$pkgver.gem
   fi
 }

 # vim:set ts=2 sw=2 et:
