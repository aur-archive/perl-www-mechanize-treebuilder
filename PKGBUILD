# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-www-mechanize-treebuilder'
pkgver='1.10003'
pkgrel='1'
pkgdesc=""
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl>=5.8.1' 'perl-html-tree' 'perl-moose>=0.65' 'perl-moosex-role-parameterized')
makedepends=('perl-test-www-mechanize')
url='http://search.cpan.org/dist/WWW-Mechanize-TreeBuilder'
source=('http://search.cpan.org/CPAN/authors/id/A/AS/ASH/WWW-Mechanize-TreeBuilder-1.10003.tar.gz')
md5sums=('3b7e1f56081fc7d41e4d38df6650cefe')
sha512sums=('7fa0893738db296e6eb8ad92e7ed0f0b42aeb19677fb15e4a8c46376ead2fb20882abf45885cc9c98611188a983e78826a3aa505f92d2a6962547b3adaeab1c0')
_distdir="WWW-Mechanize-TreeBuilder-1.10003"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
