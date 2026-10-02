# Stundera: Veröffentlichung

## Geplante Adressen
- Marketing-Website: `https://stundera.de/` (wenn diese Domain tatsächlich registriert und auf diesen Webserver gerichtet ist)
- Anwendung: `https://app.stundera.de/`

## Webserver
1. Den Inhalt dieses Repositorys im Webroot der Hauptdomain veröffentlichen. Die Startseite ist `index.html`.
2. Für den Hostnamen `app.stundera.de` als Dokumentenstamm den Ordner `/app` dieses Repositorys verwenden.
3. Im DNS für `app` den vom Webhost vorgegebenen CNAME- oder A/AAAA-Eintrag setzen. Den Zielwert beim Webhost ablesen; er ist je nach Anbieter verschieden.
4. Für beide Hostnamen HTTPS/TLS aktivieren und HTTP auf HTTPS umleiten.
5. `impressum.html` und `datenschutz.html` vor Freigabe vervollständigen. Die sichtbaren Entwurfshinweise erst entfernen, nachdem die tatsächlichen Angaben geprüft sind.

## Supabase Auth
Die Registrierung leitet Bestätigungslinks an den Ursprung der App weiter. In Supabase unter Auth URL Configuration:
- Site URL: `https://app.stundera.de`
- Redirect URL erlauben: `https://app.stundera.de/**` (oder die passende konkrete URL-Regel des Projekts)

Die Hosting-, DNS- und Supabase-Einstellungen sind Kontokonfigurationen und werden durch Dateien im Repository nicht automatisch gesetzt.

## Struktur
- Root-Dateien: öffentliche Informationsseite und rechtliche Seiten.
- `app/`: Anwendung für den separaten App-Host.
- Die App-Icons liegen zusätzlich in `app/`, damit sie bei einem eigenen Dokumentenstamm erreichbar sind.
