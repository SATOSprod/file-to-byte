# File to Byte

> 100% client-side tool to convert any file into a byte array, hex dump, or C-style `0x` hex literal directly in your browser.

**Author:** [SATOSprod](https://github.com/SATOSprod)  
**License:** MIT — see [LICENSE](./LICENSE)

---

## Features

- **Any file, any extension** — `.exe`, `.png`, files with no extension at all; every file is treated as raw bytes.
- **Three output formats:**
  - **Hex dump** — standard offset / hex / ASCII layout (like `hexdump -C`).
  - **Byte array** — comma-separated decimal array (`0-255`), ready for test fixtures.
  - **0x hex** — C-style hex literals (`0x00, 0xFF, 0xB3`), perfect for C/C++/Java/Python source code.
- **Client-side only** — files are read directly into memory via the `FileReader` API. Nothing is ever uploaded to a server.
- **Large file support** — safely loads large files (e.g., 100 MB+). A live progress bar and randomized character loading screen keep the UI responsive while reading. Dumps are capped at 2 MB for DOM performance, but exact sizes are always reported.
- **Copy and Download** — one-click copy to clipboard or download as a `.txt` file.

---

## How It Works

1. **Drop a file** into the designated drop zone, or click to open the file browser.
2. The browser's `FileReader.readAsArrayBuffer` reads the file natively.
3. For large files, a `Loading...` screen with a live percentage progress bar tracks the read operation.
4. Once loaded, click the tabs (**hex dump**, **byte array**, **0x hex**) to switch between data views.
5. Click **Copy** to copy the current view to your clipboard, or **Download .txt** to save it locally.

---

## Technical Details

- Built entirely with standard **HTML, CSS, and vanilla JavaScript**.
- **Zero dependencies** — no React, Vue, jQuery, or external libraries.
- The UI follows a strict, minimalist, programming-oriented design: no shadows, no glowing effects, and precise monospace typography.
- Fully responsive on mobile and desktop screens.

---

## File Structure

```
file-to-byte/
├── index.html        ← Structure, copy, layout, and client-side conversion logic
├── style.css         ← Minimalist flat design styles
├── favicon.svg       ← SVG logo (F2B)
└── og-image.png      ← Open Graph image for social sharing
```

---

## License

This project is released under the **MIT License**.  
See [LICENSE](./LICENSE) for full terms.

© 2026 SATOSprod
