# Road Crossing 🚗🌳

A 3D endless **"Crossy Road"-style** arcade game built with plain JavaScript and [Three.js](https://threejs.org/). Guide your character across an infinite series of grass strips and busy roads — dodge the cars and trucks, and see how far you can get.

![Three.js](https://img.shields.io/badge/Three.js-WebGL-000000?logo=three.js)
![No build step](https://img.shields.io/badge/build-none-brightgreen)

## 🎮 How to Play

| Action | Keyboard | On-screen |
|--------|----------|-----------|
| Move forward | `↑` | ▲ |
| Move backward | `↓` | ▼ |
| Move left | `←` | ◀ |
| Move right | `→` | ▶ |

- Each row you advance forward scores **+1 point**.
- You can't walk off the board edges or into trees.
- Get hit by a car or truck and it's **Game Over** — hit **Retry** to start again.

## ✨ Features

- **Procedurally generated** endless world — forests, car lanes, and truck lanes are random.
- 3D models built entirely from Three.js primitives (no external assets).
- Isometric orthographic camera that follows the player.
- Smooth animated movement with shadows and dynamic lighting.
- Works on desktop (arrow keys) and touch devices (on-screen D-pad).

## 🚀 Running Locally

Three.js is loaded from a CDN and the game uses ES modules, so it **must be served over HTTP** (opening `index.html` directly via `file://` will not work because of module/CORS restrictions).

Pick any static server:

```bash
# Python 3
python -m http.server 8000

# Node.js (npx)
npx serve .
```

Then open <http://localhost:8000> in your browser.

## 📁 Project Structure

```
.
├── index.html    # DOM: canvas, controls, score, game-over overlay
├── styles.css    # Retro "Press Start 2P" arcade styling
└── scripts.js    # All game logic (Three.js scene, generation, movement, collision)
```

## 🛠️ Tech Stack

- **Three.js** (via `esm.sh` CDN) — 3D rendering
- Vanilla JavaScript (ES modules)
- HTML5 Canvas / WebGL

## 🙌 Credits

Based on the open Three.js game tutorial at [javascriptgametutorials.com](https://javascriptgametutorials.com/).

## 📄 License

MIT
