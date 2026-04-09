# Drowsy Classics Catalog

Static catalog and media host for the Drowsy Classics mobile app.

## Structure

- `docs/catalog/v1/books.json` is the current remote catalog feed
- `docs/media/...` contains artwork and audio assets referenced by the feed

## Publishing

This repo is intended to be published with GitHub Pages from:

- branch: `main`
- folder: `/docs`

## App Config

Point the mobile app at the published feed with:

```env
EXPO_PUBLIC_CATALOG_SOURCE=remote
EXPO_PUBLIC_CATALOG_URL=https://soyster.github.io/drowsy-classics-catalog/catalog/v1/books.json
```

## Notes

- Keep book IDs stable once the app starts using them
- Keep media URLs stable even if assets are replaced
- The feed shape should match the Drowsy Classics mobile read model contract
