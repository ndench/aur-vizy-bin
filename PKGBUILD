# Maintainer: ndench
pkgname=vizy-bin
pkgver=0.5.3
pkgrel=1
pkgdesc="The most powerful virtual office ever built. An all-in-one collaboration tool to bring remote teams closer together."
arch=('x86_64')
url="https://www.vizy.io/"
depends=()
optdepends=()
license=('custom')
options=('!strip' '!emptydirs')
source=("https://releases.vizy.io/Vizy-${pkgver}.AppImage" 
        "vizy.desktop" 
	"vizy.png")
sha512sums=('946f21c54b4f99e7389338ac3482e1c8c4da44b7efe0e849f743b05fb6902fa1fd41ac0964e8e65f16309ea5c640abbdda3e4831b4925ad37e1694f150f5b4e4' 
            'a9748c196643723836417bc18fcde21dd3b1fbca5f5b505ce0f632734a3b7f93ba457d9494728ffe695be07e3701d99e75c8261a2d8b64dfb456892d0319dd72' 
	    'e9913cb05018e9efd10f7f9662933bfc4761cc468db92331fc4b21e8d8d0b661bbd3318395978f1c135872fdd01525f69bc46d4928d70f74e08bec899ce8756e')

package(){
    mkdir -p "${pkgdir}/opt/${pkgname}"
    cp Vizy-${pkgver}.AppImage "${pkgdir}/opt/${pkgname}/Vizy.AppImage"
    chmod 755 "${pkgdir}/opt/${pkgname}/Vizy.AppImage"

    install -dm755 "$pkgdir"/usr/bin
    ln -s /opt/"$pkgname"/Vizy.AppImage "$pkgdir/usr/bin/vizy"

    install -D -m644 "vizy.desktop" "${pkgdir}/usr/share/applications/vizy-desktop.desktop"
    install -D -m644 "vizy.png" "${pkgdir}/usr/share/pixmaps/vizy.png"
}
