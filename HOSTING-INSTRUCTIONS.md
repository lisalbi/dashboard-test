# OCEA University — hosting instructions (for the web manager)

This folder is a complete, self-contained web app. No build step, no database, no server code.

## What to do

1. Upload everything in this folder to a folder on the website, keeping the structure:

   ```
   /university/
     index.html
     manifest.webmanifest
     sw.js
     icons/   (5 png files)
   ```

   Example result: https://www.ocea.org/university/

2. That's it. The page must be served over **HTTPS** (ocea.org already is). Any standard web host works — there is nothing to configure.

## What members get

- Visiting the link works like a normal website.
- On a phone, "Add to Home Screen" installs it as an app: OCEA icon, full screen, works offline after the first visit.

## Updating content later

Replace `index.html` with the new version. Members pick up the update automatically the next time they open the app (the offline copy refreshes in the background). The other files only change if the icons or app name change.

## Notes

- Do not rename `index.html`, `sw.js`, or `manifest.webmanifest`.
- The app can live at any path (e.g. /university/ or /ocea-university/) — nothing inside needs editing if the path changes.
- Member quiz progress is stored on each member's own device, not on the server. Nothing about this app collects or transmits member data.
