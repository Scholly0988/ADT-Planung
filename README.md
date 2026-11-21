# Living Azeroth ADT Map Planner

Ein unabhängiges, rein clientseitiges Planungstool für neue Karten in World of Warcraft 3.3.5a (CMaNGOS). Kein Build-Prozess, keine externen Abhängigkeiten.

## Auf GitHub Pages veröffentlichen

1. Neues öffentliches GitHub-Repository erstellen (z. B. `living-azeroth-adt-planner`).
2. Die Datei `index.html` in das Hauptverzeichnis des Repositories hochladen.
3. Repository → Settings → Pages → Build and deployment: `Deploy from a branch`.
4. Branch `main`, Ordner `/(root)` auswählen und speichern.
5. Die URL ist dann in der Regel `https://BENUTZERNAME.github.io/living-azeroth-adt-planner/`.

## Bedienung

- Map-Verzeichnis: gültiger alphanumerischer Name mit Unterstrichen, entspricht dem späteren WoW-Map-Verzeichnis.
- Sichtbaren Planausschnitt in ADTs anpassen (Breite und Höhe je 1–64). Die Indizes bleiben 0–63.
- Geländetyp wählen, mit Malen/Rechteck/Füllen Kacheln anlegen. Löschen entfernt die ADT-Position aus der Planung.
- Mit „Auswählen“ eine Kachel anwählen und Bezeichnung/Notiz vergeben.
- JSON speichern und später wieder importieren. Die Anwendung speichert zusätzlich automatisch lokal im Browser (`localStorage`).
- CSV/TXT als Planungsliste und PNG als Kartenübersicht exportieren.

## Grenzen

Das Tool erzeugt keine echten `.adt`, `.wdt`, `.wdl` oder `.mpq` Dateien. Farben beschreiben Planungskategorien, keine tatsächlichen Textur- oder Höheninformationen. Der lokale Speicher ist browserspezifisch und kann gelöscht werden: regelmäßig JSON exportieren. Eine ADT misst rund 533,3333 × 533,3333 WoW-Welteinheiten und enthält 16 × 16 Terrainchunks. Pro Map existieren 64 × 64 mögliche ADT-Positionen. Für echte WotLK-ADT/WDT-Dateien sind zusätzliche Modding-Werkzeuge erforderlich.
