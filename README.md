# Scrolling-Text

A storefront-style scrolling marquee sign as a single self-contained HTML file. No dependencies, no build step, no backend — just open `index.html` in a browser.

## Features

- Type a message and display it as a full-screen scrolling sign
- Customizable text color (color picker with live hex readout)
- Adjustable scroll speed (2–30 seconds per pass)
- Shareable URLs — settings and message are encoded in query params
- Mobile-friendly with responsive font sizing and 44px+ tap targets
- Tap/click anywhere on the sign to return to the input screen

## URL Parameters

All parameters are optional.

| Parameter | Description | Example |
|-----------|-------------|---------|
| `text` | Message to display; jumps straight to scrolling view on load | `text=hello+world` |
| `color` | Text color as a 6-digit hex value (no `#`) | `color=ff0000` |
| `speed` | Seconds per pass, clamped to 2–30 | `speed=8` |

Example: `index.html?text=OPEN&color=00ff99&speed=6`

`color` and `speed` also preset the input screen even without `text`.

## Usage

Open `index.html` directly in any modern browser, or serve it from any static host.

For the **Copy shareable link** feature to work (clipboard API), the page must be served over `https://` or `localhost`. On a `file://` URL it falls back to a `prompt()` dialog.

### GitHub Pages

To get a shareable `https://` URL:
1. Push this repo to GitHub
2. Go to **Settings → Pages** and set the source to the `main` branch
3. Your sign will be live at `https://<username>.github.io/Scrolling-Text/`

## Defaults

| Setting | Default |
|---------|---------|
| Text color | `#ff7a00` (orange) |
| Scroll speed | `12s` per pass |
| Loop | Infinite |
