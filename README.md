# Labib Prompter AI — Web prototype v0.1

## Contents
- `index.html`: working prototype UI and browser speech recognition.
- `manifest.webmanifest`: install metadata.
- `sw.js`: basic app-shell cache.

## Important limitations
- Speech recognition uses the browser's SpeechRecognition / webkitSpeechRecognition implementation. Availability, Arabic dialect accuracy, and offline behavior vary by browser/device/service.
- `EXTRA_PREFER_OFFLINE` is not relevant to this web version; offline speech recognition is not guaranteed.
- Improvisation detection is heuristic: it preserves the last matching position and attempts to detect when speech no longer matches. It does not yet semantically understand improvisation or generate a reliable AI return point.
- This prototype needs to be served from HTTPS for microphone access and PWA installation. Opening `index.html` directly from a file manager may block microphone permissions.
- No audio is intentionally uploaded by this app's own code, but the browser speech-recognition provider may process audio according to its own service and privacy terms.

## Test
Deploy these files to an HTTPS static host, open the HTTPS address in Chrome on Android, grant microphone permission, paste text, choose language, prepare, and start listening. Use Chrome menu > Add to Home screen / Install app if offered.
