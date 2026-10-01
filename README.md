# Hundskram

Lokale deutsche WordPress-Installation 7.1.2.

- Website: http://127.0.0.1:8080/
- Administration: http://127.0.0.1:8080/wp-admin/
- Hauptbenutzer: Jan Behrens
- Datenbank: wp_hundskram auf dem entfernten MariaDB-Server, erreichbar über SSH-Tunnel.

## Lokal starten

In einem Terminal den SSH-Tunnel starten und geöffnet lassen:

```bash
ssh -N -o ExitOnForwardFailure=yes -L 3307:127.0.0.1:3306 root@45.133.9.76
```

In einem zweiten Terminal den Webserver starten:

```bash
cd /Users/jp.behrens/Workspace/hundskram
php -S 127.0.0.1:8080 -t .
```

Anschließend die Website öffnen. Ohne aktiven SSH-Tunnel ist die Datenbank nicht erreichbar.

Zugangsdaten stehen in wordpress-datenbank.local.md und wp-config.php. Beide Dateien sind lokal und durch .gitignore vom Einchecken ausgeschlossen. Das SSH-Passwort wird nicht gespeichert.
