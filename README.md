[README.md](https://github.com/user-attachments/files/22138279/README.md)
# Mehrere GLB-Modelle mit GitHub Pages veröffentlichen

## Ordnerstruktur
```
/ (Repo-Root)
  index.html
  /models
    models.json        ← Verzeichnis aller Modelle
    pressroststufe.glb
    pressroststufe.usdz   (optional für iOS)
    weiteres_modell.glb
```
> Sie können beliebige Dateinamen verwenden. Alle Zuordnungen passieren in `models/models.json`.

## `models/models.json` bearbeiten
Beispielinhalt:
```json
[
  { "id": "pressroststufe", "name": "Pressroststufe", "glb": "models/pressroststufe.glb", "usdz": "models/pressroststufe.usdz" },
  { "id": "teil889", "name": "Teil 889677", "glb": "models/teil889667.glb" }
]
```
- `id`: Kurzname (taucht in der URL als `?m=pressroststufe` auf)
- `name`: Anzeigename in der Liste
- `glb`: Pfad zur GLB (relativ zum Repo-Root oder absolut)
- `usdz` (optional): Pfad zur USDZ für iOS Quick Look

## Datei hinzufügen – Schritt für Schritt
1. Datei in **/models/** hochladen (z. B. `pressroststufe.glb`).
2. `models/models.json` im Browser bearbeiten und neuen Eintrag ergänzen.
3. **Commit changes**. Nach dem Pages-Deploy ist das Modell auf der Seite sichtbar.

## Direktlinks/QR
- Jede Auswahl erzeugt automatisch einen Android-AR-Link (Scene Viewer), der unten angezeigt wird.
- Sie können auch gezielt ein Modell per URL öffnen:  
  `https://<User>.github.io/<Repo>/?m=pressroststufe`

## iOS-Unterstützung (optional)
- Konvertieren Sie GLB → USDZ, laden Sie die USDZ-Datei in **/models/** hoch und tragen Sie den Pfad als `usdz` im JSON ein.
