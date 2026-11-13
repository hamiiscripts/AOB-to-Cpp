# AOB-to-Cpp

A single-page web tool that converts an Array of Bytes (AOB) pattern into a C++ byte array.

## What it does

Paste an AOB pattern such as `A1 B2 00 4F ?? 1C` and the tool outputs the C++ form, for example `0xA1, 0xB2, 0x00, 0x4F, /* ? */, 0x1C` — with `??` wildcards shown as `/* ? */`. It also shows the byte count (known bytes only) and has a COPY button to copy the output.

## How to run

No build step and no backend — it is a single static page (`index.html`, HTML + CSS + JavaScript).

- Open `index.html` directly in a browser, or serve the folder:
  ```bash
  python -m http.server
  ```
  then open http://localhost:8000
- Paste your AOB pattern, copy the C++ output.

## Notes

- The page uses Google Fonts (Orbitron) and particles.js from CDNs, so it needs internet access for its styling and effects.
- Originally developed as "SULTAN CHEAT" (see the footer in `index.html`).
