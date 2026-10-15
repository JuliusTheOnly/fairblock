# Fairblock

Block-Puzzle auf einem 8×8-Brett mit offen gelegtem Zufall. Läuft als Web-App im Browser und lässt sich auf dem iPhone zum Home-Bildschirm hinzufügen (Vollbild, offline).

**Spielen:** https://juliustheonly.github.io/fairblock/

## Auf dem iPhone installieren

1. Die Adresse oben in Safari öffnen.
2. Teilen-Symbol → „Zum Home-Bildschirm“ → „Als Web-App öffnen“ aktiviert lassen → Hinzufügen.

## So werden Steine gezogen

- 13 Formfamilien mit gleicher Chance (1/13), danach eine gleichverteilte Drehung.
- Zufall aus `crypto.getRandomValues`. Punktestand, Spielzeit und Serien haben keinen Einfluss.
- Modus **Lösbar** (Standard): Ein Dreiersatz wird nur neu gezogen, wenn sich die drei Steine in keiner Reihenfolge alle legen lassen.
- Modus **Purer Zufall**: keine Prüfung.

## Dateien

- `index.html` – das komplette Spiel (Canvas, keine Abhängigkeiten)
- `sw.js` – Offline-Cache (zuerst Netzwerk, Cache als Rückfall)
- `manifest.webmanifest`, `icons/` – Angaben für den Home-Bildschirm
