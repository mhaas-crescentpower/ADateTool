# Date Wheel Helper

This project is a small, shareable date utility focused on common date-wheel questions:

- How many weeks are between two dates?
- How many weeks until a selected month/year/day?
- What date results from adding or subtracting a number of weeks?

## Deliverable

The app is implemented as a **single self-contained HTML file**:

- `index.html` (GitHub Pages entrypoint)
- `date_tool.html` (source copy)
- `404.html` (fallback copy for GitHub Pages)
- `manifest.webmanifest` + `service-worker.js` + `app-icon.svg` (PWA install support)

No install, build, server, or dependencies are required.

## How to Run

1. Open `index.html` in any modern browser.
2. Use **Date Wheel** (default tab) for interactive spinning workflow.
3. Use **Manual Mode** tab for the three direct calculators.

## Install as App (PWA)

When hosted on GitHub Pages (HTTPS), it can be installed:

- **iPhone/iPad (Safari):** Share → **Add to Home Screen**
- **Android (Chrome):** menu → **Install app** / **Add to Home screen**
- **Desktop (Chrome/Edge):** install icon in address bar

## GitHub Pages (Simple Setup)

1. Push this folder as a GitHub repository.
2. In GitHub: **Settings → Pages**.
3. Under **Build and deployment**, choose:
	- **Source:** Deploy from a branch
	- **Branch:** `main`
	- **Folder:** `/ (root)`
4. Save. Your site will publish from `index.html`.

No build step is required.

## Maintenance Note

When updating the app, keep these files synchronized:

- `date_tool.html`
- `index.html`
- `404.html`
- `manifest.webmanifest`
- `service-worker.js`
- `app-icon.svg`

## Main UI (Date Wheel)

- Set a base date and spin weeks by dragging the wheel ring
- Also supports mouse wheel, slider, direct week entry, and quick jump buttons
- Live result panel updates instantly with target date, day shift, exact weeks, and rounded weeks
- "Snap" can align the wheel to a chosen month/year/day target in one click

## Current Logic

- Uses calendar days (`1 week = 7 days`)
- Shows both exact weeks (decimal) and rounded whole weeks
- Default rounding mode is **nearest whole week**
- For month/year calculations, target day is user-selectable (default `1`)
