# US States Game

Ein unterhaltsames, interaktives Lernspiel, bei dem du alle 50 Bundesstaaten der USA auf einer stummen Karte (Blindkarte) erraten musst. Das Spiel ist in Python geschrieben und nutzt die `turtle`-Bibliothek für die grafische Darstellung sowie `pandas` für die Datenverarbeitung.

## 🎯 Features

- **Interaktive Karte:** Jeder richtig erratene Bundesstaat wird sofort an der korrekten geografischen Position auf der Karte eingefügt.
- **Lernmodus:** Wenn du nicht weiterweißt, kannst du jederzeit "Exit" eingeben. Das Spiel beendet sich dann und erstellt automatisch eine Datei namans `states_to_learn.csv`, in der alle noch fehlenden Staaten aufgelistet sind, damit du sie gezielt lernen kannst.
- **Fortschrittsanzeige:** Ein Dialogfenster zeigt dir an, wie viele der 50 Bundesstaaten du bereits richtig erraten hast.

## 🛠 Voraussetzungen

- **Python:** Version 3.14 oder neuer
- **Paketmanager:** Das Projekt nutzt `uv` für das Abhängigkeitsmanagement.
- **Bibliotheken:**
  - `pandas` (in `pyproject.toml` bzw. `uv.lock` definiert)
  - `turtle` (ist standardmäßig bei Python dabei)

## 🚀 Installation & Start

1. **Repository klonen** oder das Projektverzeichnis öffnen.
2. **Abhängigkeiten installieren:**
   Da das Projekt `uv` verwendet, kannst du die Umgebung und alle Abhängigkeiten mit folgendem Befehl installieren:
   ```bash
   uv sync
   ```
3. **Spiel starten:**
   Sobald die virtuelle Umgebung eingerichtet ist, führe die Hauptdatei aus:
   ```bash
   uv run main.py
   ```

## 🎮 Spielanleitung

1. Nach dem Start des Skripts öffnet sich ein Fenster mit der Umrisskarte der USA.
2. Es erscheint ein Eingabedialog. Tippe den Namen eines Bundesstaates ein (z. B. "Texas", "California"). Die Groß- und Kleinschreibung wird automatisch angepasst.
3. Wenn die Antwort richtig ist, erscheint der Name des Staates auf der Karte.
4. Versuche, alle 50 Staaten zu finden!
5. **Aufgeben/Beenden:** Tippe "Exit" in das Eingabefeld ein, wenn du das Spiel vorzeitig beenden möchtest. Das Skript speichert dann die noch nicht erratenen Staaten in der neu generierten `states_to_learn.csv`-Datei im Projektordner ab.

## 📁 Dateistruktur

- `main.py`: Enthält die gesamte Logik des Spiels (Laden der Ressourcen, Spiel-Schleife, Überprüfung der Eingaben).
- `50_states.csv`: Eine Datenbank mit allen 50 US-Bundesstaaten und ihren jeweiligen x/y-Koordinaten für das Spielfenster.
- `blank_states_img.gif`: Die als Hintergrund verwendete stumme Karte der USA im GIF-Format.
- `states_to_learn.csv`: Wird generiert, wenn das Spiel vorzeitig beendet wird, und enthält alle nicht erratenen Staaten.
- `pyproject.toml` / `uv.lock`: Konfigurationsdateien für den Paketmanager `uv`.
