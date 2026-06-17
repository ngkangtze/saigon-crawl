# Saigon Crawl Navigator

A single-page, no-build navigator for the Ho Chi Minh City trip: home base, fashion boutiques, and food stops, each one tap away from turn-by-turn directions in Google Maps.

## Deploy on GitHub Pages

1. Create a new repository on GitHub (public, any name — e.g. `saigon-crawl`).
2. Upload `index.html` to the root of that repository (drag-and-drop on the GitHub web UI works, or `git add`, `git commit`, `git push` from the command line).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch", choose the `main` branch and `/ (root)` folder, then **Save**.
5. Wait about a minute, then visit `https://<your-username>.github.io/<repo-name>/`.

That's the whole setup — no build step, no dependencies to install. The page pulls Google Fonts and Leaflet (for the optional map view) from public CDNs at load time; everything else is self-contained in `index.html`.

## Editing the locations

All the location data lives in a single `DATA` array near the top of the `<script>` tag in `index.html` — each entry is a plain object with `cat`, `name`, `address`, `notes`, `lat`, `lng`, and `area`. Add, remove, or edit entries there and the list, map, and stats all update automatically.
