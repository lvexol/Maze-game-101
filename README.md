# 3D JavaScript Maze

An educational, pseudo‑3D maze game in the browser. Learn and visualize classic pathfinding algorithms as you play.

<p align="center">
  <img title="Game screen" src="https://github.com/okkindel/Labirynth/blob/master/src/assets/screens/screen.png?raw=true" width="60%" />
</p>
<p align="center">
  <img title="Game screen 2" src="https://github.com/okkindel/Labirynth/blob/master/src/assets/screens/screen2.png?raw=true" width="60%" />
</p>

---

## ✨ Highlights

* Pseudo‑3D ray‑cast style renderer
* Textured walls & ceiling with simple shading and distance fog
* Keyboard walking + mouse‑look camera
* Static 2D sprites, basic enemies with simple AI
* Health bar, damage, blood‑splash feedback
* Footstep and attack SFX, fullscreen support
* Game‑over screen with restart
* **Pathfinding lab**: 5 algorithms implemented and used by enemy AI
* Tooling: random maze generator (Java) & level editor (Python)

---

## 🚀 Quick Start

### Option A — Play from the downloaded ZIP (fastest)

1. Download the repository as a ZIP and extract it.
2. Open `index.html` in a modern browser (Chrome/Edge/Firefox).

> Some browsers restrict local file access. If assets fail to load, use the local server option below.

### Option B — Run with a local static server (recommended)

```bash
# Using Node.js (any simple server works)
npm -g i serve
serve .
# or
python3 -m http.server 8080
```

Then visit `http://localhost:3000` (or the printed port).

---

## 🎮 How to Play

* **W / A / S / D** — Move
* **Mouse** — Look around
* **Shift** — Sprint (if enabled)
* **F** — Toggle fullscreen
* **R** — Restart after game over
* **Goal** — Navigate the maze, avoid (or outrun) enemies, and reach the exit. Watch your health!

### Damage & Health

* Enemy attacks reduce health.
* Contact with bushes reduces **5 HP** per hit.
* Health is shown in the HUD. When it reaches zero — **Game Over**.

---

## 🧠 Pathfinding Algorithms

The enemy AI can be switched among five algorithms (implementation‑dependent):

* Breadth‑First Search (BFS)
* Depth‑First Search (DFS)
* Dijkstra’s Algorithm
* Greedy Best‑First Search
* A\* (A‑star)

These can be surfaced in a developer/debug menu or via config to compare behavior in real time.

---

## 🧩 Engine Features

* **Rendering**: pseudo‑3D maze from array grid; textured walls/ceilings; simple shading; distance fog
* **Input**: smooth walking, mouse camera control
* **Entities**: static 2D sprites; enemies with simple AI
* **UX**: health bar; blood splash on hit; fullscreen toggle; game over + restart
* **Audio**: footsteps; enemy attack SFX
* **Tools**: Java‑based random maze generator; Python level creator

---

## 🛠️ Tech Stack

* **Languages**: JavaScript (game), Java (maze generator), Python (level creator)
* **Rendering**: Canvas‑based pseudo‑3D (ray‑casting style)
* **Assets**: Textures & sprites bundled in `/src/assets`

---

## 📁 Project Structure (simplified)

```
/ (root)
├─ index.html
├─ src/
│  ├─ engine/        # core rendering, input, entities
│  ├─ ai/            # algorithms & enemy logic
│  ├─ levels/        # level data (generated/imported)
│  └─ assets/        # textures, sprites, audio
├─ tools/
│  ├─ generator-java/   # random maze generator
│  └─ level-editor-py/  # python level creator
└─ README.md
```

---

## 🔧 Development

1. Clone the repo: `git clone <repo-url>`
2. Install optional dev tools for live reload (e.g., Vite, parcel, or any static server).
3. Start a local server and open `index.html`.
4. Modify code in `src/` and refresh.

> If using the Java generator or Python editor, see their `README` files in `tools/` for build and usage details.

---

## 🧪 Debug & Config

* Toggle algorithm, enemy speed, fog distance, or render scale in a config file (e.g., `src/config.js`) or via a debug UI.
* Use browser devtools console for logs and quick tweaks.

---

## ❓ Troubleshooting

* **Blank screen / textures missing**: Serve via a local server instead of opening the file directly.
* **Mouse‑look not working**: Click inside the canvas to capture the pointer; ensure the page is focused.
* **Audio not playing**: Man
