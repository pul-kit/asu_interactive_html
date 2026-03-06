# Interactive Keyboard for Canvas

This repository now delivers a single self-contained webpage for a one-octave interactive piano.

## What the frontend does

- Renders a piano-style keyboard with white and black keys
- Plays a generated browser tone when a key is clicked or tapped
- Shows the last note played
- Works as a standalone static webpage with no framework runtime, backend, or API key

## Files that matter

- `index.html`: the complete app, including HTML, CSS, and JavaScript
- `canvas-embed-snippet.html`: sample iframe markup for embedding the hosted page into Canvas

## How to view it locally

You can open `index.html` directly in a browser for a quick check.

For a more realistic test, serve the folder with any static web server so the page behaves like a hosted site:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## How to use it with Canvas

Recommended approach:

1. Host `index.html` on a public HTTPS static host such as Netlify, Vercel, GitHub Pages, or a university web server.
2. Confirm the host allows iframe embedding and does not block framing with restrictive security headers.
3. Paste the iframe markup from `canvas-embed-snippet.html` into the Canvas HTML editor.
4. Replace the placeholder URL with the real hosted URL.

## Canvas notes

- Do not paste the JavaScript app directly into a normal Canvas page and expect it to run reliably.
- Canvas often sanitizes inline scripts and complex markup.
- A hosted page embedded with an iframe is the safer delivery model.
- Browser audio still requires a user interaction inside the embedded frame before sound can play.
