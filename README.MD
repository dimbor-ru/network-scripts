Mother's localhost admin presents.

This is set of crutches for automatically controlling two or more ISPs on
multihomed debian-based server. (The original system - devuan ascii.)

-	Loads nftables on start first of lan-interfaces.
-	On dhcp renew/bound (re)creates route table for each wan-interface.
-	Creates and updates list of ip-addresses for ping.
-	Pings periodically (cron) or on dhcp event and makes a list of
	available wan-interfaces.
-	Sets default route to first available wan-interface.
-	Makes disgusting beeps when switching routes and even more
	disgusting beeps when inet is not available.

Scripts are written in bash, require iproute2, nftables and dhclient.

Copyleft by dimbor <i@dimbor.ru> 2020
based on https://habr.com/ru/post/199478/
