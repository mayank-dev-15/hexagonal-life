# 🔷 Hexagonal Game of Life

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Canvas](https://img.shields.io/badge/Canvas-00C853?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![Cellular Automata](https://img.shields.io/badge/Cellular%20Automata-6A1B9A?style=for-the-badge)](https://en.wikipedia.org/wiki/Cellular_automaton)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

> Conway's Game of Life — reimagined on a hexagonal grid. Explore emergent complexity on a tessellated plane.

Hexagonal Life takes the classic cellular automaton and gives it a geometric twist. Instead of square cells with 8 neighbors, each hexagonal cell has **6 neighbors** — fundamentally changing the behavior of every rule set and producing stunning, organic patterns that feel more natural than their square-grid counterparts.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔷 **Hex Grid** | Smooth hexagonal tessellation rendered on HTML5 Canvas |
| 🎯 **Custom Rule Sets** | Define birth/survival conditions with an intuitive notation |
| 📐 **Multiple Presets** | Classic Life, Amoeba, Coral, Crystal, and more |
| 🎨 **Cell Coloring** | Age-based coloring — young cells glow, old cells fade |
| 🖱️ **Interactive Drawing** | Click and drag to paint cells onto the grid |
| ⏩ **Speed Control** | Adjust simulation speed from 1x to 60x |
| 🔄 **Wrap / Bounded** | Toggle toroidal wrapping or hard boundaries |
| 📸 **Export** | Save the current grid state as PNG or JSON |
| 📊 **Statistics** | Live population count, generation counter, and density graph |

---

## 📐 Rules

Like Conway's original, Hexagonal Life uses **Birth** and **Survival** rules — but adapted for 6 neighbors instead of 8.

### Hex Neighborhood

Each hexagonal cell has exactly **6 neighbors**:

```
    ┌───┐ ┌───┐
    │ N │ │ NE│
┌───┼───┼─┼───┤
│ NW│ ● │ │ E │
└───┼───┼─┼───┤
    │ SW│ │ S │
    └───┘ └───┘
```

### Rule Notation

Rules are written as `B/S` — which neighbor counts trigger **Birth** and **Survival**:

- **B** (Birth): A dead cell becomes alive if it has exactly N living neighbors
- **S** (Survival): A living cell stays alive if it has exactly N living neighbors

| Rule | Notation | Behavior |
|---|---|---|
| **Hex Life** | B2/S345 | Balanced — good mix of growth and stability |
| **Amoeba** | B246/S135 | Organic, blob-like growth patterns |
| **Coral** | B3/S45678 | Slow, branching coral-like structures |
| **Crystal** | B3678/S34678 | Rigid, geometric crystal growth |
| **Classic** | B3/S23 | Direct hex adaptation of Conway's original |
| **Maze** | B3/S12345 | Dense, maze-like patterns with long corridors |

### How It Differs from Square Grids

| Property | Square (8 neighbors) | Hex (6 neighbors) |
|---|---|---|
| **Connectivity** | 8 directions | 6 directions |
| **Symmetry** | 4-fold rotational | 6-fold rotational |
| **Distance** | Chebyshev metric | Axial metric |
| **Patterns** | Sharp, angular | Smooth, organic |
| **Gliders** | Common } Rarer, more complex |
| **Density** | Higher clustering | More even spread |

The hex grid's **6-fold symmetry** produces patterns that look more like natural phenomena — think honeycombs, basalt columns, or biological cell structures.

---

## 🎯 Presets

| Preset | Rule | Description |
|---|---|---|
| 🌊 **Hex Life*2 | B2/S345 | The default — balanced and exploratory |
| 🦠 **Amoeba** | B246/S135 | Organic blobs that merge and split |
| 🪸 **Coral** | B3/S45678 | Slow-growing branching structures |
| 💎 **Crystal** | B3678/S34678 | Geometric, rigid growth patterns |
| 🏰 **Maze** | B3/S12345 | Dense mazes with long corridors |
| 🔥 **Chaos** | B1/S12 | Explosive, chaotic growth |
| ❄️ **Ice** | B3678/S235678 | Frozen, stable crystal lattices |

---

## 🎮 Controls

### Simulation

| Control | Action |
|---|---|
| `Space` | Play / Pause |
| `N` | Step forward one generation |
| `R` | Randomize grid |
| `C` | Clear grid |
| `G` | Toggle grid lines |

### Drawing

| Control | Action |
|---|---|
| `Click` | Toggle cell |
| `Click + Drag` | Paint cells |
| `Right-click + Drag` | Erase cells |
| `Scroll` | Zoom in/out |
| `Middle-click + Drag` | Pan the grid |

### Settings

| Control | Action |
|---|---|
| `+ / -` | Increase / Decrease speed |
| `W` | Toggle wrap mode |
| `L` | Toggle cell age coloring |
| `S` | Export screenshot (PNG) |
| `E` | Export grid state (JSON) |

---

## 🚀 Installation

Zero dependencies — runs entirely in the browser.

```bash
# Clone the repository
git clone https://github.com/mayank-dev-15/hexagonal-life.git

# Open in your browser
cd hexagonal-life
open index.html
```

Or simply open `index.html` directly from your file system.

---

## 🎮 Usage

1. **Choose a preset** from the dropdown menu (or define custom rules)
2. **Draw cells** by clicking and dragging on the grid
3. **Press Space** to start the simulation
4. **Adjust speed** with `+` / `-` keys
5. **Experiment** with different rule sets to discover new patterns
6. **Export** your favorite patterns as PNG or JSON

**Tips:**
- Start with the **Hex Life** preset and a small cluster of cells
- Try the **Crystal** preset for mesmerizing geometric growth
- Use **Maze** with a randomized grid for complex labyrinths
- Toggle **wrap mode** to create seamless infinite patterns

---

## 🔬 About Cellular Automata

A **cellular automaton** is a discrete model studied in mathematics, physics, and theoretical biology. It consists of:

- **Grid** — a regular lattice of cells (square, hexagonal, etc.)
- **States** — each cell is in one of a finite number of states (alive/dead)
- **Neighborhood** — a definition of which cells are "neighbors"
- **Rules** — a function that determines the next state based on current state and neighbors

### History

- **1940s** — Stanislaw Ulam and John von Neumann pioneer the concept
- **1970** — John Conway invents the Game of Life (square grid, B3/S23)
- **1980s** — Stephen Wolfram classifies 1D cellular automata into 4 classes
- **2000s+** — Hexagonal variants gain popularity for their natural aesthetics

### Why Hexagons?

Hexagonal grids are the **most efficient way to tile a plane** with equal-area cells while minimizing perimeter. They appear everywhere in nature:

- 🐝 Honeycombs
- 🪨 Basalt columns (Giant's Causeway)
- 🧬 Biological cell packing
- 🌍 Geographic mapping (H3, S2)
- 🎮 Board games (Settlers of Catan, Civilization)

In cellular automata, hex grids produce **more isotropic** (directionally uniform) behavior because all 6 neighbors are equidistant — unlike square grids where diagonal neighbors are √2 times farther.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<p align="center">
  Built with ❤️ by <a href="https://github.com/mayank-dev-15">mayank-dev-15</a> — exploring emergence, one hex at a time.
</p>
