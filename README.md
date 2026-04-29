# oauth-bridge

Static HTML bridge pages that catch OAuth2 callbacks from providers requiring HTTPS redirect URIs and bounce them to iOS apps' custom URL schemes via `window.location.replace`.

iOS's `ASWebAuthenticationSession` then catches the custom-scheme redirect.

## Live pages

- `https://alphabtc.github.io/oauth-bridge/improved-wakeup-time-callback/` — bridges to `improvedwakeup://oauth-callback?...`

## Adding a new bridge

1. Create a new directory `<app-name>-callback/` at the repo root.
2. Copy any existing `index.html` into it.
3. Replace the `improvedwakeup://oauth-callback` literal with your app's custom scheme + path.
4. Commit and push. GitHub Pages serves it within a minute.
