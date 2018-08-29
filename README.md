# ccu-addon-redis

[![Current Release](https://img.shields.io/github/release/hobbyquaker/ccu-addon-redis.svg?colorB=4cc61e)](https://github.com/hobbyquaker/ccu-addon-redis/releases/latest)
[![Github Releases](https://img.shields.io/github/downloads/hobbyquaker/ccu-addon-redis/total.svg)](https://github.com/hobbyquaker/ccu-addon-redis/releases)

[Redis](https://redis.io/) als Addon für die
[Homematic CCU3](https://www.eq-3.de/produkte/homematic/zentralen-und-gateways/smart-home-zentrale-ccu3.html) und 
[RaspberryMatic](https://github.com/jens-maus/RaspberryMatic)

Unter [Releases](https://github.com/hobbyquaker/ccu-addon-redis/releases) steht die Datei 
`redis-<version>.tar.gz` zum Download zur Verfügung, diese kann über das CCU WebUI als Zusatzsoftware installiert
werden.

Eigene Konfigurationen können in `/usr/local/addons/redis/etc/local.conf` vorgenommen werden, der Inhalt dieser Datei
wird bei Updates nicht überschrieben.

Redis ist eine schnelle Datenbank, die einfache Datensätze aufnehmen kann und alle Inhalte im Hauptspeicher hält. Dadurch werden alle Kommandos in höchster Geschwindigkeit ausgeführt. Redis ist keine SQL-Datenbank! Die Daten aus dem Hauptspeicher können auf einem Speichermedium abgelegt werden. 
Redis wird hauptsächlich als einfacher schneller Datenspeicher für Datenhalt und, Caches oder für Message broker eingesetzt.

Die Datensätze bestehen immer aus einem Schlüssel (Beispiel: "Messpunkt-201808011543") und einem Wert (Beispiel: "34,5 Grad"). Schlüssel und Wert sind üblicherweise vom Typ String.
Kommandos sind z.B. get, set und del.
Beispiel: 
redis> set Messpunkt-201808011543 34,5 Grad
OK
redis> get Messpunkt-201808011543
34,5 Grad
redis> del Messpunkt-201808011543
(integer) 1
