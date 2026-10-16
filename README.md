# Our Little Home — Cloudflare edition

## Included
- `index.html`: existing app UI updated to load a room-specific illustrated background.
- `assets/rooms/`: illustrated background files for the entrance, library, living room, kitchen, bedroom, annex, letters, and seasonal themes.
- `manifest.json`, `icon.svg`: PWA metadata/icons (when present in the source package).

## Publish the static PWA
1. Upload the contents of this folder to a GitHub repository, keeping the `assets` folder next to `index.html`.
2. In Cloudflare, open **Workers & Pages → Create → Pages → Connect to Git** and select the repository.
3. For a plain static site, set the build command to blank and the output directory to `/` (or use the repository root, depending on the Cloudflare setup screen).
4. Deploy, then open the `*.pages.dev` URL.

## Important current limitations
This package applies the room illustrations as visual backgrounds. It does **not** yet connect cross-device accounts, shared real-time chat, private annex permissions, or photo storage. Those require a Worker API, D1 database, and R2 bucket configuration plus authentication and access-control code. The current prototype's local-only functions should not be treated as shared cloud data.

## Asset note
The room artwork is cropped from the approved concept-board image to make separate background files. Some original mockup labels/UI are therefore part of the decorative background; actual app controls are layered above them.
