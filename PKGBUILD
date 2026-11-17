# Maintainer: Timofey Brukhanchik <asyncbtd@gmail.com>
# Contributor: Marcin Nowak <marcin.j.nowak+aur # gmail DOT com>
# Contributor: Koi Dong <akillcool#live.com>
# Contributor: Sergei Marochkin <me@ziggi.org>
# Contributor: Morris Jobke <morris.jobke AT gmail DOT com>
# Contributor: Boris Shomodjvarac <shomodj AT gmail DOT com>
# Contributor: G. Richard Bellamy <rbellamy@pteradigm.com>

pkgname=dbschema
pkgver=10.6.0
pkgrel=1
pkgdesc='Relational Data Browse, Query Builder, SQL Editor, schema deployment and synchronization.'
arch=('i686' 'x86_64')
url='http://www.dbschema.com/'
license=('custom')
source=(
    "${pkgname}-${pkgver}.tar.gz::https://dbschema.com/download/dbschema_linux_${pkgver//./_}.tar.gz"
    "dbschema.desktop"
    "https://dbschema.com/img/favicon/favicon.svg"
)
# verify here: https://dbschema.com/download/md5sums
md5sums=('667e1954ba49ac6ab06942dd8739c2a0'
         'fd70b65c057119c0290bf9f4b51be830'
         'd969120667f2e5050f98be6d8b37a042')

package() {
    install -dm755 "${pkgdir}/opt"
    cp -r DbSchema "${pkgdir}/opt/${pkgname}"

    chmod 755 "${pkgdir}/opt/${pkgname}/DbSchema"
    install -Dm644 "${pkgname}.desktop" "${pkgdir}/usr/share/applications/${pkgname}.desktop"
    install -Dm644 "favicon.svg" "${pkgdir}/opt/$pkgname/favicon.svg"
    install -dm755 "${pkgdir}/usr/bin"
    ln -s "/opt/${pkgname}/DbSchema" "${pkgdir}/usr/bin/dbschema"
}
