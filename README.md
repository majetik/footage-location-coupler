# Footage Location Coupler

A one-button phone web app for vlogging. Press **Pin!** when you start recording, and it saves the exact time (to the second, with timezone) and your GPS position. Later you can match clips to places by their timestamps.

## Features
- One big Pin button. The time is captured the instant you tap; GPS fills in a moment later.
- GPS stays warm while the app is open, so most pins are instant. A chip shows accuracy (±m).
- Map with numbered pins and a dashed route in the order you filmed.
- Add a note to each pin (clip name, what you filmed).
- If GPS fails (subway, indoors), the pin keeps its time and you can tap **Place on map**.
- Export as CSV (spreadsheet), GPX (Google Earth, Lightroom, DaVinci, etc.), or JSON backup, and restore from a backup.
- Works offline after the first load. Map tiles you've already viewed are cached.
- All data stays on the phone (localStorage). Nothing is sent anywhere.

## Files
- `index.html`: the whole app
- `sw.js`: offline caching
- `manifest.webmanifest`, `icon*.png`, `icon.svg`: lets you "Add to Home Screen"

## Hosting
Phones only allow GPS on HTTPS pages, so it needs a static host. Any one works (GitHub Pages, Netlify, Cloudflare Pages). No build step.

## Tips for the trip
- **Add it to your home screen** (Safari: Share > Add to Home Screen). On iPhone, Safari can clear a website's storage after 7 days without a visit; home-screen apps are exempt.
- **Export a JSON backup every evening.** Your pins exist only on the phone until you do.
- **Check your camera's clock** matches your phone (set it to Japan time on arrival). Clip timestamps and pin times must agree for matching to work.
