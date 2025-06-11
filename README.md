# LM Studio KI Coder

Dieses Tool aktualisiert automatisch Quellcode-Dateien in einem Verzeichnis mithilfe einer lokalen KI (z. B. LM Studio + LLM). Unterstützt werden viele Programmiersprachen wie Python, C++, JavaScript, Rust u. v. m.

## ✨ Funktionen

- Lokale Verarbeitung über LM Studio (kein Cloud-Zwang)
- Unterstützung für zahlreiche Programmiersprachen
- Backups aller bearbeiteten Dateien
- Individuell anpassbarer Prompt

---

## 🧠 Voraussetzungen

- [LM Studio](https://lmstudio.ai) installiert und gestartet
- Ein passendes LLM-Modell ist geladen und als **lokaler Chat-Endpunkt** erreichbar:

```Link

[http://localhost:1234/v1/chat/completions](http://localhost:1234/v1/chat/completions)

````

> Tipp: In LM Studio unter „API“ den lokalen Server aktivieren und Port 1234 verwenden.

---

## 🛠 Installation

1. **Python 3.8+** installieren (falls noch nicht vorhanden)
2. Erforderliche Pakete (nur Standard-Libraries werden genutzt)
3. Repository klonen oder Dateien lokal speichern
4. Programm starten:

 ```bash
 python KI-Code-Updater.py
````

---

## 🚀 Verwendung

1. **Arbeitsverzeichnis** wählen (z. B. ein Projektordner mit `.py`, `.js` usw.)
2. **Programmiersprache** auswählen
3. **Prompt anpassen** (optional)

   * Platzhalter `{language}` und `{code}` werden automatisch ersetzt
4. Auf **„Code aktualisieren“** klicken
5. Ergebnis abwarten – Fortschrittsbalken zeigt den Status an

> ✅ Alle bearbeiteten Dateien werden vorher gesichert (Ordner `backups/` im jeweiligen Quellverzeichnis).

---

## 🔧 Beispiel-Prompt

```text
Aktualisiere diesen {language}-Code:
- Ersetze veraltete oder unsichere Syntax
- Behalte die Funktionalität bei

Code:
{code}
```

---

## 📁 Unterstützte Sprachen & Dateiendungen

| Sprache    | Endung  |
| ---------- | ------- |
| Python     | `.py`   |
| JavaScript | `.js`   |
| C++        | `.cpp`  |
| Rust       | `.rs`   |
| Java       | `.java` |
| Bash       | `.sh`   |
| HTML       | `.html` |
| …          | …       |

> Die vollständige Liste wird dynamisch aus dem internen Mapping erzeugt.

---

## ❓ Fehlersuche

* **„API-Fehler: Verbindung abgelehnt“** → Ist LM Studio aktiv und auf Port 1234?
* **Keine Dateien gefunden** → Verzeichnis korrekt gewählt? Sprache und Dateiendung stimmen überein?

---

