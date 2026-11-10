# Slotgun — Web release

Play: https://realcraig.github.io/lucky-number-strip/

Finished Unity Web export, published by `.github/workflows/pages.yml`.
The data file is stored in ordered parts below GitHub's Git file-size limit.
The workflow joins `BuildParts/export.data.unityweb.*` into
`_site/Build/export.data.unityweb` and verifies `BuildParts/SHA256SUMS` before deployment.
Only the reconstructed export is published; the parts are not downloaded by players.

For a new release, replace `index.html`, `og-image.png`, `Build/` and `TemplateData/`
from the fresh Unity export. Split the data file into 90,000,000-byte parts,
update its SHA-256 manifest, and remove the unsplit data file from `Build/` before committing.
Do not ship `*_BurstDebugInformation_DoNotShip` folders.

Map data © OpenStreetMap contributors (ODbL). Elevation from USGS 3DEP lidar (public domain).
Casino names and logos are parodies.
