# Acausal Sound Healing (PWA)

A browser-based sound healing tool that uses:

- Vector-aware chat intake (understands emotions, pain locations, energy level, focus, environment, etc.)
- Optional bio tracking (HR, HRV, sleep, stress)
- Platonic solids + Tetrateron (star-matrix) harmonics
- Pink-noise carrier fields + toroidal LFO modulation
- 4-6-8 coherence breathing
- Before/after tracking of subjective state
- Progressive Web App (PWA) support for installability
- Light / dark theme toggle
- Optional voice input for the chat (Web Speech API, where supported)

All processing runs locally in the browser using the Web Audio API. No data is sent to any server.

## What is a PWA?

A Progressive Web App (PWA) is a web application that can be:

- Installed to your home screen (like a native app)
- Launched full-screen without the browser chrome
- Given basic offline capability via a service worker

This project includes:

- `manifest.webmanifest` – tells browsers how to install / display the app
- `service-worker.js` – caches the core files so the app can still open if your network is flaky

## Usage

1. Open `index.html` in a modern browser (Chrome, Safari, Edge, Firefox).
   - On GitHub Pages, you can just visit the published URL.
2. Use the chat to describe how you feel and what you want from the session.
3. Optionally enable bio data and fill in HR, HRV, sleep, stress.
4. Adjust fine-tune controls (ancient mode, aura color, environment, session length) if desired.
5. Run the 4-6-8 breathing coach.
6. Click **Start sound field** to begin the pink-noise + harmonic geometry session.
7. After the session, rate how you feel and save the outcome to build a personal history.

### Voice input

If your browser supports the Web Speech API (e.g., Chrome on desktop or some Android browsers):

- Tap the 🎙 button next to the chat box.
- Speak your state or intention.
- The recognized text will be sent through the same vector-aware engine as typed input.

If voice is not supported on the device, the app will gently tell you in the chat.

## Development

This is a static project – there is no build step required.

- Just open `index.html` directly in a browser, or
- Serve the directory with a small HTTP server for local testing:

```bash
python -m http.server 8080
# then open http://localhost:8080 in your browser
```

When hosted over HTTPS (for example, on GitHub Pages), the PWA features (service worker, install prompt)
will be available in compatible browsers.

## Tech stack

- HTML / CSS / JavaScript (no framework)
- Web Audio API
- [three.js](https://threejs.org/) for 3D geometry visualization
- Web Speech API (optional, for voice input)
- PWA: manifest + service worker

## License

You can choose your preferred license (MIT, proprietary, etc.).
