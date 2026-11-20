# Pelgrimsmarathon – routeplanner

Web-app om marathonetappes langs de officiële pelgrimsroute naar Santiago de Compostela uit te zetten
en als GPX te delen met WorkOutDoors op de Apple Watch, plus een gedeeld logboek van gelopen etappes.

Live: https://route.pelgrimsmarathon.nl

## Opbouw

- `index.html` – de complete app
- `manifest.webmanifest`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png` – app voor het beginscherm
- `etappes/etappes.json` – lijst met gelopen etappes
- `etappes/*.gpx` – de gelopen tracks (met tijden; tijd, tempo, hoogtemeters en hartslag worden in de app berekend)
- `etappes/fotos/` – eventueel foto's (handmatig te uploaden via github.com)
- `CNAME` – eigen domein

## Gelopen etappe toevoegen

Voeg een GPX toe in `etappes/` en een regel in `etappes/etappes.json`:

```json
{
  "nr": 1,
  "titel": "Roosteren – Maastricht",
  "datum": "2026-11-28",
  "van": "Roosteren",
  "naar": "Maastricht",
  "lopers": ["Siebren", "…"],
  "gpx": "etappes/etappe-01.gpx",
  "verslag": "Tekst van het verslag.\n\nNieuwe alinea.",
  "fotos": ["etappes/fotos/01-start.jpg", "https://…/foto.jpg"],
  "album": "https://link-naar-gedeeld-fotoalbum",
  "videos": ["https://youtu.be/…"],
  "strava": "https://www.strava.com/activities/…",
  "links": [{ "titel": "Krantenartikel", "url": "https://…" }]
}
```

Alle velden behalve `nr` en `gpx` zijn optioneel.

Gepubliceerd via GitHub Pages (branch `main`, map `/`). Routedata © OpenStreetMap-bijdragers (ODbL).
