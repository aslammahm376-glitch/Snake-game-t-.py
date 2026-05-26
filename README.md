# 🐍 Snake Game

A classic Snake Game built with **Python** and **Pygame**, featuring smooth graphics, animated sprites, sound effects, and a real-time score tracker. This project demonstrates object-oriented programming principles and game loop architecture in a clean, well-structured codebase.

![Game Screenshot](screenshot.png)

---

## 📖 Table of Contents

- [About the Project](#about-the-project)
- [How It Works](#how-it-works)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [How to Run](#how-to-run)
- [Controls](#controls)
- [Screenshots](#screenshots)
- [Future Improvements](#future-improvements)
- [License](#license)

---

## 🎮 About the Project

This is a fully functional Snake Game where the player controls a snake that grows longer each time it eats an apple. The game ends if the snake collides with the walls or its own body. It features directional sprite graphics for the snake's head, body, and tail — giving it a polished, animated look beyond a typical colored-block snake game.

---

## ⚙️ How It Works

The game is built around three core classes:

- **`SNAKE`** — Manages the snake's body as a list of `Vector2` positions. Handles movement logic, directional graphic selection (head/body/tail), block growth, and sound playback on fruit consumption.
- **`FRUIT`** — Randomly places an apple on the grid. If an apple spawns on the snake's body, it re-randomizes its position automatically.
- **`MAIN`** — The game controller. Coordinates updates, collision detection, failure conditions, rendering, and score display.

Each game tick (triggered by a Pygame timer event every 150ms), the snake moves one cell in its current direction. Collision with a wall or self triggers a reset. Eating an apple grows the snake, updates the score, and plays a crunch sound.

---

## ✨ Features

- 🐍 **Smooth Snake Movement** — Direction-aware sprite rendering with distinct head, body, and tail graphics that change based on the snake's travel direction and turns.
- 🍎 **Randomized Food Spawning** — Apple appears at a random cell each time it is eaten, never overlapping the snake's body.
- 🏆 **Live Score System** — Score is displayed in the corner with an apple icon, updating in real time as the snake grows.
- 💀 **Game Over & Auto-Reset** — The game detects wall collisions and self-collisions, then smoothly resets without requiring a restart.
- 🔊 **Sound Effects** — A satisfying crunch sound plays each time the snake eats an apple.
- 🌿 **Checkered Grass Background** — A dynamically drawn checkerboard pattern gives the board a clean, polished visual style.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **Python 3.x** | Core programming language |
| **Pygame** | Game rendering, event handling, audio |
| **pygame.math.Vector2** | 2D position and direction math |

---

## 📦 Installation

Follow these steps to set up the project on your local machine.

**1. Clone the repository**
```bash
git clone https://github.com/your-username/snake-game.git
cd snake-game
```

**2. Create and activate a virtual environment** *(recommended)*
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

**3. Install dependencies**
```bash
pip install pygame
```

**4. Verify the project structure**

Make sure your project directory looks like this:
```
snake-game/
├── snake_game.py
├── Graphics/
│   ├── apple.png
│   ├── head_up.png
│   ├── head_down.png
│   ├── head_left.png
│   ├── head_right.png
│   ├── tail_up.png
│   ├── tail_down.png
│   ├── tail_left.png
│   ├── tail_right.png
│   ├── body_vertical.png
│   ├── body_horizontal.png
│   ├── body_tr.png
│   ├── body_tl.png
│   ├── body_br.png
│   └── body_bl.png
├── Sound/
│   └── crunch.wav
└── Font/
    └── PoetsenOne-Regular.ttf
```

---

## ▶️ How to Run

```bash
python snake_game.py
```

The game window will open at **800×800 pixels** (20×20 grid, 40px per cell). The snake starts stationary — press any arrow key to begin.

---

## 🕹️ Controls

| Key | Action |
|---|---|
| `↑` Arrow Up | Move snake up |
| `↓` Arrow Down | Move snake down |
| `←` Arrow Left | Move snake left |
| `→` Arrow Right | Move snake right |

> The snake cannot reverse directly into itself — opposite-direction inputs are ignored.

---

## 📸 Screenshots

### Gameplay

![Snake Game Gameplay](screenshot.png)

> *The snake navigates the checkered board toward the apple. Score is displayed in the bottom-right corner.*

---

## 🚀 Future Improvements

- [ ] **Main Menu & Game Over Screen** — Add a proper start screen and a "Game Over" overlay with the final score before resetting.
- [ ] **High Score Persistence** — Save and display the all-time high score using a local file or SQLite database.
- [ ] **Difficulty Levels** — Let the player choose speed (Easy / Medium / Hard) before starting.
- [ ] **Multiple Fruits** — Spawn more than one apple, or add special bonus items with time limits.
- [ ] **AI Snake Mode** — Implement a pathfinding algorithm (e.g., A* or BFS) to auto-play the game.
- [ ] **Responsive UI** — Pause menu, mute button, and in-game settings panel.
- [ ] **Leaderboard** — Multiplayer or online high-score board.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

*Built with 🐍 Python and Pygame*
