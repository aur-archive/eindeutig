# Contributor: Michael P <ptchinster@archlinux.us>

pkgname=eindeutig
pkgver=20050628_1
pkgrel=2
pkgdesc="Examine the contents of Outlook Express DBX email repository files (forensic purposes)."
arch=('i686' 'x86_64')
url="http://www.jonesdykstra.com/"
license=('GPL')
source=("http://downloads.sourceforge.net/project/fast/Eindeutig/Eindeutig%20v20050628_1/eindeutig_$pkgver.zip")
md5sums=('efc16a5fe63347dd5f4454b840f68057')
 
prepare(){
    cd "$srcdir/eindeutig_$pkgver/src"
    mv Eindeutig.c eindeutig.c
}
 
build() {
    cd "$srcdir/eindeutig_$pkgver/src"
    make
}
  
package() {
    cd "$srcdir/eindeutig_$pkgver/src"
    #Base directories
    install -dm755 "$pkgdir/usr/bin/"
 
    #Binaries
    #renaming to dbxparse as the usage is for dbxparse not eindeutig
    install -m755 ../bin/eindeutig "$pkgdir/usr/bin/dbxparse"
}

