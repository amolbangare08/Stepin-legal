# Step-In — legal

The two documents Google Play requires for the Step-In Android app, hosted on GitHub Pages.

| Page | Where it is used |
|---|---|
| `privacy.html` | Play Console → Store listing → Privacy policy |
| `delete-account.html` | Play Console → Data safety → Data deletion |
| `index.html` | Links to both |

They live in their own repository rather than in the app's, because turning on Pages for that one
would publish its whole `docs/` folder — including notes on the server the app talks to.

## Keeping them in step

The sources are in the app repository, and edits belong there first:

- `docs/privacy-policy.html` — a fragment meant to be pasted into a host, so the copy here is
  wrapped in `<!doctype html>`, `<head>` and `<body>`
- `docs/store/delete-account.html` — already a standalone page, copied across unchanged

Play re-checks both URLs after publication. A 404 here is an enforcement action on the listing, so
this repository stays public and these paths do not move.
