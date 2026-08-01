# Мои курочки

Offline egg/chicken-coop tracker for a non-technical caretaker. Single
self-contained `index.html` (HTML + CSS + vanilla JS, no build step, no
dependencies), installable as a PWA via `manifest.json` + `sw.js`.

## Run it

Just open `index.html` in a browser (works from `file://`, no server
needed). To test the "install to home screen" / offline-caching behavior,
serve the folder over HTTP or HTTPS (service workers don't register under
`file://`), e.g.:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000/chicken-tracker/`.

## Data

Everything is stored in `localStorage` under the key `kurochkiData_v1`, one
record per calendar day. The in-app "Копия данных" / "Восстановить" buttons
export/import that state as plain text for manual backup.
