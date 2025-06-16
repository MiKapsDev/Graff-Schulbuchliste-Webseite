# Schulbuchbestellung – Uploadformular für Buchhandlung Graff

Dieses Repository stellt ein responsives HTML/CSS-Frontend zur Verfügung, mit dem Kunden der Buchhandlung Graff ihre Schulbuchliste über ein Onlineformular einreichen können. Es ist vorbereitet für die Integration mit serverseitiger Logik zur Weiterverarbeitung per Mail. Anpassungen an das bisherige System und Verarbeitung im Backend muss noch entsprechend erfolgen.

## Dateien

- `index.html`: Enthält das Formular mit allen notwendigen Feldern
- `styles.css`: Enthält ein modernes, responsives Layout, abgestimmt auf das CI der Graff Webseite
- `send_mail.php`: Muss von externem Dienstleister bereitgestellt/angepasst werden

## Hinweise für Integration

### Backend

- Das Formular erwartet ein `send_mail.php`, welches folgende Felder verarbeitet:
  - `vorname`, `nachname`, `strasse`, `hausnummer`, `plz`, `ort`, `birthdate`, `email`, `lieferung`, `nachricht`
  - `bilder[]` (nur Bilddateien)
- Das Backend sollte:
  - Validierung auf erlaubte Dateitypen&#x20;
  - E-Mail-Versand der Daten (z. B. via PHPMailer)
  - Fehlerbehandlung (z. B. ungültige Eingaben, Upload zu groß etc.)

---

*Stand: Juni 2025 – Entwickelt für die Buchhandlung Graff, Braunschweig.*

