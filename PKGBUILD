# Maintainer: Eric Ozwigh <com dot gmail at ozwigh>

pkgname=scenebuilder-bin
pkgver=8.0.0
pkgrel=2
pkgdesc="A Visual Layout Tool for JavaFX Applications (binary version)"
provides=scenebuilder
conflicts=scenebuilder
arch=('any')
depends=('java-openjfx')
url='http://gluonhq.com/products/tools/scene-builder'
license=('BSD')
source=('SceneBuilder-8.0.0.jar::http://gluonhq.com/download/scene-builder-8-0-0/'
        'scenebuilder.sh')
noextract=("${source[@]%%::*}")
sha1sums=('ec7e69ec6e135938c13db298db0467b28105644f'
          'cbcb8d249f98efec4247e79d0f08c161432b9afd')

package() {
	install -dm755 "$pkgdir/usr/share/java/scenebuilder"
	install -Dm644 "$srcdir/SceneBuilder-8.0.0.jar" "$pkgdir/usr/share/java/scenebuilder"
	ln -s "/usr/share/java/scenebuilder/SceneBuilder-8.0.0.jar" "$pkgdir/usr/share/java/scenebuilder.jar"
	install -Dm755 "$srcdir/scenebuilder.sh" "$pkgdir/usr/bin/scenebuilder"
}
