# Keeping the front page current

This app is one of the apps on https://mgilvryallen.github.io/ (repo `mgilvryallen/mgilvryallen.github.io`).
The front page shows the `description` in this app's `manifest.webmanifest`, read live, so the
manifest is where this app describes itself to the world.

Whenever a change adds, removes or renames something a person using the app would notice, update
in the same commit:

- `description` in `manifest.webmanifest`: one to three plain sentences on what the app does and
  its main features, in the same voice as the README. It is also the install prompt's text.
- the matching `<meta name="description">` in `index.html` (same text).
- the README's feature list.

If you can also reach the front page repo, update this app's fallback `about` line in its `APPS`
list to match (it's only shown if the manifest can't be read).

## Changing the icon

Browsers keep icons a long time. When the icon changes, re-render the PNGs from `icons/icon.svg`
and bump the `?v=` on every icon address: in `index.html` (the `rel="icon"` and
`apple-touch-icon` links and the header image) and in `manifest.webmanifest`. The front page
takes this app's icon from the manifest, so it picks up the new one too. Bump `CACHE` in
`sw.js` as well.
