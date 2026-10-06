# 🌀 Spiral

A collection of minimalist animated spiral / circle visualizations rendered on an HTML5 canvas.
Pure HTML + CSS + JavaScript. No dependencies. No build step. Just open and watch.

Perfect for:
- Ambient background visuals 🌌
- Screensavers / wallpapers
- Learning canvas animation, easing, and Web Audio API
- Hypnotizing yourself at 3 AM 😵‍💫

---

## 🔗 Live Demos

| # | Preview | Description |
|---|---------|-------------|
| 1 | [**index.html**](https://lodo4ka-the-best.github.io/Spiral/index.html) | ⚪ White circles on black — smooth growing circles, epic sound |
| 2 | [**index2.html**](https://lodo4ka-the-best.github.io/Spiral/index2.html) | 🌀 White spiral with a live settings panel (radius, speed, line width) |
| 3 | [**index3.html**](https://lodo4ka-the-best.github.io/Spiral/index3.html) | 🌀 White spiral, continuous drawing, epic audio-reactive drone |

---

## 📄 index.html — White Circles

Draws concentric white circles on a black background, one by one. Each circle is drawn with an eased animation, and the cursor smoothly travels to the start of the next one.

### Features
- ⚪ Infinite growing circles
- 🎬 Smooth `easeInOutCubic` animation for both drawing and cursor movement
- 🔵 Adaptive segment count (128 → 720) for high-quality large circles
- 🔊 "Epic" sound: low drone + sweep on draw start + hit on circle finish
- 🔁 Restart button + live circle counter
- 📱 Hides UI on phones in landscape mode

### Controls
- **↺ Начать заново** — restart the animation
- **🔊 Эпичный звук** — toggle sound on/off
- **Click anywhere** — unlocks audio context (browser autoplay policy)

---

## 📄 index2.html — Spiral with Settings

Draws a white spiral on a black background, with a **live settings panel** where you can tweak parameters on the fly.

### Features
- 🌀 Continuous spiral drawing from the center
- ⚙️ Floating settings panel with sliders
- 🎚️ Real-time parameter adjustment
- 📊 Live counters: revolutions and current radius
- 🔁 Restart button
- 📱 Responsive: mobile-friendly layout
- 🚫 Hides all UI on phones in landscape mode

### Settings
| Parameter | Range | Description |
|-----------|-------|-------------|
| **Start radius** | 0 – 50 px | Radius of the very first point |
| **Radius growth** | 1 – 50 px/turn | How much the radius increases per revolution |
| **Draw speed** | 0.01 – 0.2 rad/frame | Angular speed of the drawing cursor |
| **Line width** | 1 – 8 px | Thickness of the spiral line |

Click **🔄 Применить и перезапустить** to apply the changes and restart the spiral.

### Controls
- **⚙ Настройки** — show / hide the settings panel
- **↺ Начать заново** — restart with the current settings

---

## 📄 index3.html — Epic Spiral

A fixed-configuration, continuous white spiral on a black background, tuned for a cinematic feel with reactive audio.

### Features
- 🌀 Continuous, ever-growing white spiral
- 🔵 High-quality rounded line with soft glow (via `shadowBlur`)
- 🔊 **Reactive audio**:
  - Low drone whose frequency and gain follow the current radius
  - Triangle-wave "tick" on every completed revolution
- 🎬 Frame-rate independent drawing (uses `deltaTime`)
- 🧠 Buffer limited to 100 000 points for stable performance
- 📱 Hides UI on phones in landscape mode
- 🖱️ Auto-starts audio on first click / touch / after 500 ms

### Fixed Parameters
```js
const START_RADIUS  = 5;   // Initial radius
const RADIUS_GROWTH = 5;   // Radius increase per revolution
const DRAW_SPEED    = 1;   // Angular speed (rad per frame at 60 FPS)
const MAX_SEGMENTS  = 720; // (kept for compatibility)
```

### Controls
- **↺ Начать заново** — restart the spiral
- **🔊 Эпичный звук** — toggle sound on/off

---

## 🚀 Running Locally

No build tools needed. Just clone and open:

```bash
git clone https://github.com/LODO4KA-THE-BEST/Spiral.git
cd Spiral
```

Then open any of the files in your browser:

```
index.html
index2.html
index3.html
```

Or serve them with any static server:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

---

## 🛠️ Tech Stack

- **HTML5 Canvas 2D** — all rendering
- **Web Audio API** — sound synthesis (drone + sweeps + ticks)
- **Vanilla JS** — no frameworks, no libraries
- **CSS** — glassmorphism-style UI overlay

---

## 🧠 What You Can Learn From This Repo

- Canvas drawing with `requestAnimationFrame`
- Frame-rate independent animation via `deltaTime`
- Easing functions (`easeInOutCubic`)
- Adaptive geometry (segment count based on radius)
- Web Audio API: oscillators, gains, frequency ramps
- Glassmorphism UI with `backdrop-filter`
- Responsive design with orientation-specific media queries

---

## 📜 License

Do whatever you want with it. Attribution is nice but not required. ✨
