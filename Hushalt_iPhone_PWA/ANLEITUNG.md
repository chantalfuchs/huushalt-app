# 🏡 Was hend mir im Hushalt? – iPhone-App

Das ist eine **Progressive Web App (PWA)** auf Basis deines Claude-Artefakts. Kein App Store, keine Anmeldung innerhalb der App und kein kostenpflichtiges Apple-Entwicklerkonto nötig.

## Enthaltene Dateien
- `index.html`: deine Haushalts-App mit Food, Non-Food, Einkaufsliste, Mengen und Kategorien; plus Backup-Export/-Import
- `manifest.webmanifest`: App-Name und Icon
- `service-worker.js`: lädt die App nach dem ersten Besuch grundsätzlich auch offline
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`: App-Icons

## Kostenlos online stellen mit GitHub Pages (am Computer)
1. Öffne https://github.com und melde dich an oder erstelle ein kostenloses Konto.
2. Klicke oben rechts auf **+ → New repository**.
3. Repository-Name z. B. `hushalt-app` eingeben, **Public** auswählen und **Create repository** klicken.
4. Klicke **uploading an existing file** (oder **Add file → Upload files**).
5. Lade **alle sechs Dateien** aus dem entpackten Ordner hoch, **direkt ins Hauptverzeichnis** des Repositorys. Nicht nur die ZIP hochladen! `README.md` ist optional. Klicke **Commit changes**.
6. Öffne im Repository **Settings → Pages**. Bei **Build and deployment** wähle **Deploy from a branch**, Branch **main**, Ordner **/(root)** und **Save**.
7. Warte, bis GitHub Pages die veröffentlichte Website-Adresse unter **Settings → Pages** anzeigt. Sie sieht normalerweise wie `https://DEIN-NAME.github.io/hushalt-app/` aus.

## Auf dem iPhone installieren
1. Öffne **Safari** (nicht den Browser innerhalb einer anderen App).
2. Rufe die unter GitHub Pages angezeigte HTTPS-Adresse auf und prüfe, dass deine Liste angezeigt wird.
3. Tippe auf **Teilen** (Quadrat mit Pfeil) → **Zum Home-Bildschirm**. Falls ausgeblendet: in der Teilen-Liste weiter nach unten scrollen.
4. Als Name z. B. `Hushalt` wählen und, falls angeboten, **Als Web-App öffnen** aktivieren. Auf **Hinzufügen** tippen.
5. Öffne das Haus-Icon auf dem Home-Bildschirm. Teste einen Artikel und die Einkaufsliste. Schalte danach testweise den Flugmodus ein und öffne die App erneut.

## Wichtig zu deinen Daten
- Dein Vorratsstand, neue Produkte und Kategorien werden per `localStorage` **nur auf diesem iPhone in dieser installierten App** gespeichert.
- **Keine Synchronisation** mit deinem Computer oder anderen Geräten. Safari und die Home-Bildschirm-App können getrennte Speicherbereiche haben.
- Mache regelmässig ein Backup über **⬇️ Backup speichere** und bewahre die JSON-Datei in der Dateien-App/iCloud Drive auf. Mit **⬆️ Backup lade** kannst du sie wiederherstellen.
- Wenn du die App oder deren Website-Daten entfernst, können die lokal gespeicherten Daten verloren gehen. Eine Neuinstallation garantiert nicht, dass sie noch vorhanden sind.
- Dein GitHub-Repository und damit **die im HTML enthaltene ursprüngliche Produktliste** sind bei einem öffentlichen Repository sichtbar. **Spätere persönliche Änderungen auf dem iPhone werden nicht nach GitHub hochgeladen.** Keine vertraulichen Daten in den Quellcode eintragen.
- Offline-Betrieb funktioniert nach dem ersten vollständigen Online-Laden und erfolgreicher Service-Worker-Installation. Extern geladene Google-Schriftarten können offline durch Systemschriften ersetzt werden.

## Spätere Aktualisierung
Bei Änderungen an HTML/CSS/JavaScript Dateien im Repository ersetzen bzw. committen. Für Offline-Aktualisierungen gegebenenfalls den Cache-Namen in `service-worker.js` von `hushalt-pwa-v1` auf `hushalt-pwa-v2` ändern; nach erneutem Online-Öffnen wird die neue Version geladen. Sichere deine Daten vor grösseren Änderungen.
