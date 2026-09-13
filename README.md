# Native Site Locations of Southern New England

An interactive map of 1,282 Native American archaeological sites in Massachusetts, Rhode Island
and Connecticut, plus 252 places whose names carry a Native presence.

Sources: the Bulletin of the Massachusetts Archaeological Society, Vols. 1–83 (1939–2022), and the
Massachusetts Historical Commission Reconnaissance Survey town reports.

## Publishing this with GitHub Pages

1. Create a repository — call it whatever you like, e.g. `native-sites`.
2. Upload everything in this folder, keeping the structure:
   ```
   index.html
   data/native_sites.csv
   data/native_place_names.csv
   data/native_sites.kml
   data/native_sites_mymaps.kml
   README.md
   ```
   Drag and drop works: on the repo's front page use **Add file → Upload files**, then drop the
   whole folder in.
3. Go to **Settings → Pages**.
4. Under *Build and deployment*, set **Source** to *Deploy from a branch*, **Branch** to `main`
   and the folder to `/ (root)`. Save.
5. Wait a minute or two. The page appears at:
   ```
   https://<your-username>.github.io/<repository-name>/
   ```

`index.html` is completely self-contained — no libraries, no build step, nothing to install. It
pulls only its basemap tiles, from OpenStreetMap, which is why it needs to be served from a real
web address rather than opened out of a file preview.

## Using the map

- **Location confidence** — strong, medium, weak. Weak means the survey called the site *probable*:
  a terrace, a pond shore, a river reach where sites were expected, not one that was dug.
- **Show error-margin circles** — every pin carries a radius in metres. A pin is only as good as
  its circle.
- **Record** — MAS Bulletin against MHC town report, and a filter for the placements that have
  been checked against a named source.
- **Native place names** — a separate layer: teal diamonds for Algonquian names, purple for English
  names recording a Native presence. Names label themselves as you zoom in.
- **Hide legend** — collapses the panel so the map fills the window.
- Click any pin or name for its record, with links out to Google Earth and satellite view.

## The data

`data/native_sites.csv` is the source of truth. `location_basis` says how each point was placed and
names the source where one was found; `version_note` marks the placements that have been
source-checked. All 999 MHC-derived placements have now been checked, which moved 210 pins, 182 of
them by over a kilometre.

`data/native_sites_mymaps.kml` is organised into 8 layers for import into Google My Maps;
`data/native_sites.kml` is the fuller version for Google Earth, foldered by record and town with
the error margins as circles on the ground.
