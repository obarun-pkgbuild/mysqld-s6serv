# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=mysqld-s6serv
pkgver=0.1
pkgrel=2
pkgdesc="mysqld service for s6"
arch=(x86_64)
license=('beerware')
depends=('mariadb' 's6' 's6-rc' 's6-boot')
conflicts=()
install=mysqld-s6serv.install
source=('mysqld.daemon.run.s6'
		'mysqld.log.run.s6'
		'LICENSE')
md5sums=('a0de584f8a4d06072f2fe26e3c59dd47'
         'c77dd78d7d260d527b538923b854c987'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/mysqld.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/mysqld/run"
	
	# log
	install -Dm 0755 "$srcdir/mysqld.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/mysqld/log/run"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/mysqld-s6serv/LICENSE"
}
