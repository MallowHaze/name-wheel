## Live
- Live site: [Wheel - Spin](https://mallowhaze.github.io/name-wheel/)

# Wheel - Spin 🎡

A lightweight, mobile-first “spin the wheel” name picker built as a single-page web app and hosted on GitHub Pages.  
Designed for non-technical users: open → tap the center → get a winner.
> Note: if a device shows an older version after an update, open the site with a cache-buster like `?v=13` (or any higher number), then refresh.

---

## Features
- **Max 8 names** (wheel automatically scales to the number of filled names)
- **Spin by tapping the center** (“SNURRA”)
- **Swedish UI** for everyday use
- **Winner highlight** (pulse) + **subtle confetti**
- **Install support**
  - Android: install prompt supported (where available)
  - iOS: manual “Share → Add to Home Screen” (expected limitation)
- **Theme**
  - **System (auto)** / Light / Dark
  - System mode follows phone theme changes automatically
- **Optional settings**
  - Sound (off by default)
    - Click-click-click spin sound
    - Winner ding
    - Individual toggles under **Avancerat**
  - History (last 5 winners)
  - Lock editing (prevents accidental edits)

---

## Install / Add to Home Screen
### Android (Chrome / Edge / Samsung Internet)
- Tap **Installera** in the app (or browser menu → Install app).

### iPhone / iPad (Safari)
- Tap **Share** → **Lägg till på hemskärmen**.
- iOS does not support the Android-style install prompt.

---

## Privacy / Storage
- Names, settings, and optional history are stored **locally on each device** (LocalStorage).
- No accounts, no tracking, no external services.

---

## Project structure
- `index.html` — full app (UI + logic)
- `manifest.json` — PWA metadata
- `sw.js` — service worker caching
- `icon-192.png`, `icon-512.png` — app icons
- `wheel-spin-icon-1024.png` — optional hi-res icon (convenience)

---

## Versioning
This project uses a simple app-style versioning:

- **App version**: tracked in this README changelog (vX.Y.Z).
- **Cache buster**: the `?v=13` query you append to the URL when you want to force-refresh a device cache after updates.

They are related, but not the same thing.

---

## Changelog

### v1.3.0 — PWA + Themes + Install button + Wheel SFX
- Added PWA support (`manifest.json`, icons, service worker)
- Added **Installera** button:
  - Uses install prompt where supported
  - Shows iOS instructions otherwise
- Added theme selection: **System / Light / Dark**
  - System mode follows OS theme changes
- Added sound system (off by default):
  - Click-click-click spin sound (toggle in Avancerat)
  - Winner ding (toggle in Avancerat)
- Removed redundant spin button (center tap is primary)
- Added “advanced settings” section
- General UI polish and mobile-first layout improvements

### v1.2.0 — Delight features
- Added winner highlight pulse
- Added subtle confetti effect
- Added optional history (last 5 winners)
- Added optional lock editing

### v1.1.0 — Name editing + Swedish UI
- Added name editor (one per line)
- Enforced max 8 names
- Wheel scales to number of filled names (no empty segments)
- Translated UI to Swedish for accessibility

### v1.0.0 — Initial release
- Basic wheel spinner
- GitHub Pages deployment
- Winner display

---

## Development notes
### Caching
If you update the app and a device still shows an old version:
1. Open the live site with a new cache-buster query, e.g. `?v=14`
2. Refresh
3. If installed as a home-screen shortcut, remove it and add again from the updated URL

### iOS install limitation
iOS requires “Add to Home Screen” via Safari Share menu. This is expected behavior.
