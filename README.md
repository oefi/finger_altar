# ▲ ALTAR — Who Goes First?

> The board-game first-player ritual. Everyone places a finger. One is chosen.

![altar](https://github.com/user-attachments/assets/5214cc3b-cde6-412a-bdfc-c8d860eab615)

## What it is

A single HTML file you open on a phone or tablet and lay flat on the table.  
No app store. No install. No backend. No framework. Save the file once, works offline.

Players place their fingers on the screen simultaneously. A sonar-style countdown locks everyone in. A slot-machine animation cycles through all fingers with exponential slowdown — then one is chosen.

Takes about 15 seconds. Creates about 15 seconds of genuine tension.

---

## How to use

1. Open `index.html` in any mobile browser  
   — or use the [live demo](https://oefi.github.io/finger_altar/)
2. Tap **Add to Home Screen** for true fullscreen (recommended)
3. Lay the device flat on the table
4. Everyone places a finger
5. Hold until the timer locks in
6. Watch the ritual unfold

**Controls** (top-right corner):
- 🔊 — toggle sound on/off
- ⛶ — fullscreen (Android/Chrome only; iOS use Add to Home Screen)

---

## Features

- Up to **10 simultaneous players** (iPad/Android tablet hardware limit)
- **Sonar screensaver** — ghost fingerprints teach the UI without instructions
- **Perimeter countdown timer** — visible from all sides of the table
- **Slot-machine selection** — winner chosen by RNG before animation starts
- **Collision-aware winner overlay** — text flips to avoid covering the winning finger
- **▲ AGAIN button** — instant re-run from the winner screen
- **Sound toggle** — mutable Web Audio synthesis, zero audio files
- **PWA / Add to Home Screen** — installs with correct name, icon, fullscreen mode
- **prefers-reduced-motion** — respects OS accessibility settings
- **visibilitychange** — timer pauses on phone calls / tab switches
- Mouse fallback for desktop testing

---

## Tech

| Thing | Reality |
|---|---|
| File count | 1 |
| Dependencies | 0 |
| Framework | none |
| Build step | none |
| Backend | none |
| Audio files | none |
| Total size | ~22 KB |

Web Audio API (synthesized oscillators) · Touch Events API · CSS custom properties · SVG `stroke-dashoffset` timer · RequestAnimationFrame loop · Web App Manifest (inline data URI)

---

## Development

No build toolchain. Open the file. Edit the file. Reload.

```bash
# Serve locally if you need it
npx serve .
# or
python3 -m http.server
```

All constants (timer duration, winner display time, player colors) are at the top of the `<script>` block.

---

## Repo structure

```
altar.html          ← the entire app
altar-preview.png   ← OG image / README screenshot
README.md
LICENSE
docs/
  changelog.md
  workflow-prompts.md
```

---

## License

MIT — see [LICENSE](LICENSE)
