# Italiano 500 – Intermedio 🇮🇹

Eine **eigenständige**, mobile Italienisch-Lernapp (A2 → B1), optimiert für iPhone und Safari.

## Funktionen

- 500 **Wörter und alltagstaugliche Wendungen** (nicht 500 unterschiedliche Einzelwörter), in 20 Themen mit je 25 Einträgen
- 12 Dialoge mit 48 Gesprächsbeiträgen und deutscher Übersetzung
- Italienische Sprachausgabe (Web Speech Synthesis), normales und langsames Tempo
- Optionale Spracherkennung über Web Speech API, sofern der Browser sie unterstützt
- Karteikarten, 10-Fragen-Quiz, Wiederholungssystem (1/3/7/14/30 Tage)
- Tägliche Einheiten von etwa 10 Minuten, 30-Tage-Kalender, Statistiken
- Kurze Grammatik- und Spanisch-Hinweise
- PWA mit Offline-Cache für App-Dateien; Spracheingabe kann online erforderlich sein
- Lernfortschritt lokal im Browser, JSON-Export/-Import

**Hinweis:** Spracherkennung bewertet nur erkannte Wörter, nicht die phonetische Aussprache. Sie kann auf iPhone/Safari fehlen. Für die Sprachausgabe muss eine italienische Stimme auf dem Gerät verfügbar sein. Das Angebot ist keine zertifizierte CEFR-Niveaustufenprüfung.

## Veröffentlichung auf GitHub Pages

1. ZIP entpacken.
2. Auf https://github.com/new ein **öffentliches** Repository `italiano500` erstellen.
3. Unter **Add file → Upload files** den **Inhalt** des entpackten Ordners in die Wurzel des Repositories hochladen und committen. `index.html` muss direkt im Repository liegen.
4. **Settings → Pages → Build and deployment → Deploy from a branch**, Branch `main`, Ordner `/(root)` auswählen, **Save**.
5. Nach dem Deployment öffnen: `https://DEIN-GITHUB-NAME.github.io/italiano500/`.
6. In iPhone Safari **Teilen → Zum Home-Bildschirm** wählen.

GitHub Pages verwendet HTTPS, das für PWA und Mikrofon wichtig ist. Das Repository ist unabhängig von deiner Beginner-App. Keine Zugangsdaten oder API-Schlüssel nötig.

## Lokal testen

Im Projektordner `python3 -m http.server 8000` starten und im Browser `http://localhost:8000` öffnen. Die App nicht über `file://` öffnen, da dann `fetch()` blockiert werden kann.

## Dateien

- `index.html` – Einstieg
- `style.css` – mobiloptimiertes Design
- `app.js` – Logik, Quiz, Dialoge, Sprache und Statistiken
- `words.json` – 500 Wendungen und Kategorien
- `manifest.webmanifest` – PWA-Metadaten
- `sw.js` – Offline-Cache
- `icon.svg`, `icon-192.png`, `icon-512.png` – App-Symbole

## Datenschutz & Einschränkungen

Der Lernstand liegt in `localStorage` auf dem jeweiligen Gerät und wird nicht mit der Beginner-App synchronisiert. Website-Daten können gelöscht werden; deshalb regelmäßig exportieren. Spracherkennung kann vom Browser/OS über externe Dienste verarbeitet werden. Die Anwendung selbst hat keinen Server und verschickt keine Lerndaten. Inhalte sind als praktische Gesprächsbausteine kuratiert, nicht als nach Häufigkeit berechnete Top-500-Wortliste. Der Offline-Cache deckt die App-Dateien ab, nicht notwendigerweise die Browser-Sprachdienste.

## Hinweis zur Umbenennung

Die internen Lernstand- und Sicherungskennungen bleiben zur Kompatibilität mit der vorherigen Intermedio-Version unverändert. Die Veröffentlichung und PWA-Pfade sind relativ und funktionieren unter `/italiano500/`.
