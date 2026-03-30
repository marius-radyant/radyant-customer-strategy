# Customer Strategy Flowchart – Projektkontext

## Überblick
Interaktiver HTML-Flowchart für Radyant (Organic Growth Agency), der die Kundenstrategie als Decision Tree abbildet. Ursprünglich für Bi-Weekly Kundencalls konzipiert, jetzt breiter als generelles Kundenstrategie-Framework.

## Datei
- `biweekly-call-flowchart.html` (Single-File HTML mit inline CSS + JS)
- Gehostet auf GitHub Pages: `https://marius-radyant.github.io/customer-strategy/`

## Tech-Stack
- Reine HTML/CSS/JS, kein Framework
- SVG-Connector-Lines via JavaScript (Bezier-Kurven mit Pfeilmarkern)
- Absolute-positioned `div`-Nodes mit CSS-Klassen für Typen
- Zoom/Pan via CSS `transform: scale()`
- Canvas: 5400×4800px

## Radyant Brand
- Primary: `#7b55f4` (Lila)
- Secondary: `#f2eefe` (Helles Lila)
- Success: `#7a9c59` (Grün)
- Alert: `#e31f11` (Rot)
- Font: Inter / system fallback

## Node-Typen (CSS-Klassen)
- `n-start` – Lila, pill-shaped, Startpunkt
- `n-end` – Grüner Gradient, pill-shaped, Endpunkt
- `n-decision` – Helles Lila mit Lila Border, Entscheidungsfragen
- `n-green` – Grün, positive Aktionen
- `n-red` – Rot, Probleme/Korrekturen
- `n-orange` – Orange, Warnungen/Überprüfungen
- `n-blue` – Blau, analytische Schritte
- `n-purple` – Lila, strategische Aktionen
- `n-principle` – Dunkel Lila, Grundprinzipien (Begründungspflicht)
- `n-neutral` – Weiß mit hellem Lila Border

## Connection-Typen
- `'g'` – Grün (Ja/positiv)
- `'r'` – Rot (Nein/negativ)
- `'n'` – Neutral/Lila

## Flowchart-Struktur

### Gemeinsamer Pfad (oben, Mitte)
1. **Start** → Kundenstrategie starten
2. **Leads/Revenue/Purchases** – Branchenziele
3. **Ziele definiert?** (Decision) → Nein: Ziele festlegen / Ja: weiter
4. **Ziele relevant?** (Decision, inkl. strategische Veränderungen beim Kunden) → Nein: anpassen / Ja: weiter
5. **Reporting-Zugriff?** (Decision) → Nein: einrichten / Ja: weiter
6. **On Track / Off Track?** (Decision) → verzweigt

### Off Track (links)
- Off Track → Ursachenanalyse → Richtiger Ansatz? → (Nein links: Ansatz ändern | Ja rechts: Proxy prüfen) → Alle Maßnahmen bewerten

### On Track (rechts)
- On Track → Attribution auf Radyant zurückführbar? → (Nein: Impact klären | Ja: weiter) → Erfolgstreiber identifiziert? → (Nein: Reporting verbessern | Ja: Learnings nutzen) → Maßnahmen prüfen → Effizienz prüfen

### Konvergenz (Mitte unten)
- **Begründungspflicht** (einzelner breiter Node, 680px, beide Pfade münden hier)
- → Confirm / Revise Content Plan
- → Offene Punkte klären
- → Action Items & Nächste Schritte (End)

## Wichtige Design-Entscheidungen
1. **Ziele VOR Reporting** – Ziele geben Kontext, was gemessen wird
2. **Attribution** sowohl bei Zieldefinition als auch als On-Track-Checkpoint
3. **Strategische Veränderungen** in Ziel-Relevanz-Check integriert (nicht separat)
4. **Begründungspflicht** als einzelner Konvergenz-Node (nicht doppelt pro Pfad)
5. **Ja/Nein-Konsistenz**: Ja immer rechts (grün), Nein immer links (rot)
6. **"Wichtig:"-Callouts** als `<span class="node-callout">` (bold, mit Abstand)

## Bekannte Pitfalls
- Title-Bar überlappt Start-Node wenn `padding-top` fehlt (min. 80px)
- Center-Column Decision Nodes müssen konsistente `left`-Werte haben
- Miro-Integration wurde versucht, funktioniert schlecht (leere Nodes) – verworfen
- GitHub Pages braucht `index.html` als Dateinamen oder expliziten Pfad in URL
