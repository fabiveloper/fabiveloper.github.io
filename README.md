# fabiveloper.github.io

Schlichte statische Website für Fabian Unger. Die Website besteht ausschließlich aus direkt bearbeitbaren HTML-Dateien, einer CSS-Datei und einem SVG-Symbol.

Kein React, kein TypeScript, kein JavaScript, kein Python-Generator, keine npm-Pakete und kein Build-Schritt. `LegalScreen.tsx` und andere App-Dateien gehören nicht in dieses Repository und sind nicht enthalten.

## Dateien

```text
index.html                      Startseite, Projekte, Kontakt
simulation.html                 Rennbahn-Projekt
family-tree.html                App-Beschreibung
impressum.html                   Anbieterangaben mit Platzhaltern
datenschutz.html                 Website-Datenschutz
datenschutz-family-tree.html     App-Datenschutz
404.html                        Fehlerseite
assets/style.css                Gesamtes Design
assets/favicon.svg              Website-Symbol
robots.txt                      Indexierung nicht erwünscht
.nojekyll                       Keine Jekyll-Verarbeitung
.github/workflows/pages.yml     Optionaler, gesperrter Pages-Upload
```

## Lokal öffnen und bearbeiten

ZIP entpacken und `index.html` im Browser öffnen. Alle relativen Links und Styles funktionieren ohne Server. Texte direkt in den HTML-Dateien bearbeiten, das Design in `assets/style.css`.

Optional für einen lokalen Server: `python -m http.server 8000` im Ordner ausführen und `http://localhost:8000` öffnen. Python ist nur für diesen optionalen lokalen Server nötig, nicht für die Website.

## GitHub Pages

Ziel ist das User-Repository `fabiveloper.github.io` im Konto `fabiveloper`. Die Website ist noch nicht auf GitHub veröffentlicht worden.

1. Vorhandene Website-Dateien sichern. Wenn du das erste Paket schon hochgeladen hast, nicht einfach beide Versionen mischen: Hier gibt es kein `dist/`, `src/`, `scripts/`, `content/`, `templates/`, `app-integration/` oder `site.config.json` mehr.
2. Den Inhalt dieses Ordners in die Wurzel des Website-Repositorys übernehmen, nicht in einen zusätzlichen Unterordner. Keine Family-Tree-App, Signierschlüssel oder Test-Stammbäume hochladen.
3. Vor Veröffentlichung die drei Rechtsseiten vollständig ergänzen und auf die tatsächliche Hosting-/Vertriebssituation abstimmen.
4. GitHub: Settings → Pages → Source: GitHub Actions.
5. Erst nach Freigabe: Settings → Secrets and variables → Actions → Variables → Repository variable `PAGES_RELEASE_APPROVED` auf `true` setzen.
6. Vor Veröffentlichung die `Platzhalter:`-Angaben in den Rechtsseiten vervollständigen. Die Seiten verwenden derzeit `noindex,nofollow`; für die fertige Website diese Einstellung anpassen. `robots.txt` dann auf `Allow: /` umstellen.
7. Den Workflow „Publish static HTML (gated)“ manuell starten. Er kopiert nur HTML, Assets, robots.txt und .nojekyll, ohne Compiler oder Generator.

Die variable Freigabe und die Textprüfung sind redaktionelle Schutzmaßnahmen, keine automatische Rechtsprüfung. Es gibt keinen automatischen Deploy bei jedem Push. Ein leerer oder nicht auf `true` gesetzter Schalter lässt den Job aus. Manuelle Veröffentlichung oder die GitHub-Einstellung „Deploy from a branch“ würden diese Sperre umgehen.

`noindex` und `robots.txt` sind kein Zugriffsschutz. Dateien in einem öffentlichen Repository sind öffentlich, auch wenn Pages nicht aktiviert ist.

## Noch offene Rechtsangaben

Insbesondere ladungsfähige Anschrift, zusätzlicher geeigneter unmittelbarer Kontaktweg, gegebenenfalls Register-/USt-/Wirtschafts-ID-Angaben, GitHub-Hostingkonstellation (Empfänger, Übermittlungen, Fristen), Support-E-Mail-Verarbeitung und App-Store-Vertrieb sind noch zu ergänzen. Die Texte sind keine Garantie für Rechtskonformität.

Die Website enthält weder Tracker noch externe Fonts, Einbettungen oder Formulare. GitHub Pages verarbeitet beim Aufruf dennoch Verbindungsdaten. Diese Website ist eine Projektpräsentation, kein Shop und keine Zahlungsabwicklung.

## Verbindung zur App

Die bestehenden LegalScreen-Links bleiben gleich:

- `https://fabiveloper.github.io/impressum.html`
- `https://fabiveloper.github.io/datenschutz-family-tree.html`

Diese Adressen werden erst nach Einrichtung und Veröffentlichung erreichbar. Der bereits separat gelieferte LegalScreen bleibt ausschließlich im App-Repo. Seine offline gespeicherten Texte müssen bei relevanten Änderungen separat aktualisiert und mit einem App-Update ausgeliefert werden; dieses Website-Repo erzeugt keine App-Dateien mehr.

## Prüfung

Lokale Verweise, Assets, fehlende Skripte, mobile Darstellung und Navigation wurden geprüft. Für den finalen Rechtsstand und das App-Verhalten sind gesonderte Prüfungen erforderlich.
