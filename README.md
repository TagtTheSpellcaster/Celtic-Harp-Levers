# Celtic Harp Levers

![Version](https://img.shields.io/badge/version-1.3.1-amber.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![PWA](https://img.shields.io/badge/PWA-ready-success.svg)
![Offline](https://img.shields.io/badge/offline-supported-brightgreen.svg)
![Dependencies](https://img.shields.io/badge/dependencies-none-lightgrey.svg)

A clean, high-contrast visual Progressive Web App (PWA) for lever harpists to quickly look up and verify sharping lever positions on a Celtic harp tuned in **E-flat Major ($E\flat$)** (with all levers disengaged/down).

---

## Features

- **Circle of Fifths Key Selector:** Instant access to all 8 standard major keys (from $3\flat$ to $4\sharp$) and their relative minor keys, complete with treble clef key signatures.
- **Visual String & Lever Board:** Color-coded octave strings (Red for C, Blue for F, Natural for D, E, G, A, B) paired with animated mechanical levers showing exact UP (engaged) and DOWN (open) positions.
- **Real-Time Sounding Pitch Display:** Shows both the open string note and the actual sounding pitch resulting from the current lever state.
- **Interactive Lever Toggling:** Click or tap any individual lever to test custom, modal, or non-standard configurations.
- **Bilingual & Dual Notation Switch:** Single-click toggle between **English** (`C D E F G A B` / `UP`–`DOWN`) and **Italian** (`Do Re Mi Fa Sol La Si` / `SU`–`GIÙ`).
- **Offline-First PWA:** Installable on mobile, tablet, and desktop devices with full offline caching via Service Worker. Zero external dependencies.

---

## Lever Chart Reference ($E\flat$ Base Tuning)

Starting from the standard $E\flat$ Major tuning (all levers **Down**), engaging levers one by one following the Circle of Fifths yields 8 major keys and their relative minors:

| Key Signature | Major Key | Relative Minor | C (Do) | D (Re) | E (Mi) | F (Fa) | G (Sol) | A (La) | B (Si) |
| :--- | :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **$3\flat$** | $E\flat$ Major | C Minor | Down | Down | Down | Down | Down | Down | Down |
| **$2\flat$** | $B\flat$ Major | G Minor | Down | Down | Down | Down | Down | **Up** | Down |
| **$1\flat$** | F Major | D Minor | Down | Down | **Up** | Down | Down | **Up** | Down |
| **$0$** | C Major | A Minor | Down | Down | **Up** | Down | Down | **Up** | **Up** |
| **$1\sharp$** | G Major | E Minor | Down | Down | **Up** | **Up** | Down | **Up** | **Up** |
| **$2\sharp$** | D Major | B Minor | **Up** | Down | **Up** | **Up** | Down | **Up** | **Up** |
| **$3\sharp$** | A Major | $F\sharp$ Minor | **Up** | Down | **Up** | **Up** | **Up** | **Up** | **Up** |
| **$4\sharp$** | E Major | $C\sharp$ Minor | **Up** | **Up** | **Up** | **Up** | **Up** | **Up** | **Up** |

---

## Project Structure

```text
.
├── index.html       # Main application markup, styles, and logic
├── manifest.json    # PWA web app manifest
├── sw.js            # Service worker for offline caching
├── icon-192.png     # PWA home screen icon (192x192)
├── icon-512.png     # PWA splash/store icon (512x512)
└── README.md        # Project documentation
```

---

## Installation & Deployment

1. **Local Development:** Because Service Workers require HTTP/HTTPS, serve the directory using any local static server (e.g., `npx serve .` or `python3 -m http.server 8080`) rather than opening `index.html` directly via `file://`.
2. **Hosting:** Deploy all files to any static HTTPS host (such as GitHub Pages, Netlify, or Vercel).
3. **Install as App:** Open the hosted URL in Chrome, Safari, Edge, or Firefox and select **"Install App"** or **"Add to Home Screen"**.

---

## License

This project is licensed under the **MIT License**.
