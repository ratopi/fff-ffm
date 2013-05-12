# scripts.ffm

Dieses Verzeichnis enthält Scripte, die den Build-Prozess vereinfachen und unterstützen sollen.

Die Scripte wurden für das Frankfurter Freifunk-Netz erstellt, lassen sich aber eventuell auch für andere Freifunk-Netze verwenden.


## clean-build.sh

Das Script führt die für ein Build notwendigen Schritte aus.


## tag-the-next-release.sh

Dieses Script legt ein Tag mit der nächsten Versionsnummer an.
Die Schritte im einzelnen:

* Abfrage der gewünschten Versionsnummer und nächsten Snapshot-Versionsnummer. Das Script schlägt hierbei die Versionsnummern vor, die normalerweise passen sollten; falls nicht können sie geändert werden.
* Änderung der Dateien, die die Versionsnummer enthalten: Setzen der nächsten Version
* Commit der Änderungen
* Tagging mit der gewählten Versionsnummer
* Änderung der Dateien, die die Versionsnummer enthalten: Setzen der nächsten Snapshot-Version
* Commit der Änderungen

Danach steht im neuen Tag, die getaggte Version zur Verfügung und kann mit

	git checkout <Versionsnummer>

ausgecheckt werden.

Der master enthält immer eine SNAPSHOT-Version mit der vorraussichtlichen nächsten Versionsnummer als Basis.

**Achtung!!!** Das Script führt momentan **kein** Git-Push aus.  Der Befehl

	git push <Versionsnummer>

sollte daher zeitnah nach dem Ausführen des Scripts durchgeführt werden.

