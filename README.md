# 🚀 Space Shooter Game

> A **classic 2D space shooter game** built with C++ demonstrating object-oriented programming principles. Features dynamic enemy spawning, collision detection, and progressive difficulty.

<div align="center">

![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![OOP](https://img.shields.io/badge/OOP-Game%20Design-blue?style=flat-square)
![Gameplay](https://img.shields.io/badge/Gameplay-Action-brightgreen?style=flat-square)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)

[Features](#features) • [Getting Started](#getting-started) • [Controls](#controls) • [Gameplay](#gameplay) • [Architecture](#architecture)

</div>

---

## ✨ Features

- **Classic Gameplay** - Intuitive space shooter mechanics
- **Enemy Waves** - Progressive difficulty with increasing enemy spawns
- **Collision Detection** - Accurate hit detection for bullets and enemies
- **Score System** - Points for destroying enemies
- **Lives System** - Multiple lives before game over
- **Power-ups** - Special items to enhance gameplay
- **OOP Architecture** - Well-structured object-oriented design
- **Smooth Animation** - Real-time graphics rendering
- **Game States** - Menu, playing, paused, game over screens

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| **Language** | C++17 |
| **Graphics** | Raylib 4.5+ |
| **Architecture** | Object-Oriented Design |
| **Build System** | CMake / Makefile |

---

## 📁 Project Structure

```
Space_shooter_CPP/
├── 📂 src/                      # Source code
│   ├── main.cpp                 # Game entry point
│   ├── game.cpp                 # Main game loop
│   ├── player.cpp               # Player character
│   ├── enemy.cpp                # Enemy logic
│   ├── bullet.cpp               # Projectile system
│   ├── collision.cpp            # Collision detection
│   └── button.cpp               # UI buttons
│
├── 📂 include/                  # Header files
│   ├── game.h
│   ├── player.h
│   ├── enemy.h
│   ├── bullet.h
│   ├── entity.h
│   └── button.h
│
├── 📂 assets/                   # Game resources
│   ├── sprites/
│   ├── sounds/
│   └── textures/
│
├── 📄 CMakeLists.txt           # CMake configuration
├── 📄 Makefile                 # Make configuration
└── 📄 README.md                # This file
```

---

## 🚀 Getting Started

### Prerequisites

- **C++17 or later** compiler (GCC, Clang, MSVC)
- **CMake** 3.10+ or **Make**
- **Raylib** graphics library
- **Git** for version control

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/MuhammadHammadCS/Space_shooter_CPP.git
cd Space_shooter_CPP
```

#### 2. Install Raylib

**On Ubuntu/Debian:**
```bash
sudo apt-get install libraylib-dev
```

**On macOS (with Homebrew):**
```bash
brew install raylib
```

**On Windows:**
- Download from [Raylib Website](https://www.raylib.com)
- Follow installation instructions

#### 3. Build the Project

**Using CMake:**
```bash
mkdir build
cd build
cmake ..
cmake --build .
```

**Using Make:**
```bash
make
```

#### 4. Run the Game

```bash
./SpaceShooter
# or
./build/SpaceShooter
```

---

## 🎮 Controls

| Key | Action |
|-----|--------|
| **W / ↑** | Move up |
| **A / ←** | Move left |
| **S / ↓** | Move down |
| **D / →** | Move right |
| **Space** | Fire bullets |
| **P** | Pause/Resume |
| **ESC** | Back to menu / Quit |
| **R** | Restart game (after game over) |

---

## 🎯 Gameplay

### Objective
Destroy enemy spacecraft while avoiding their fire to survive as long as possible.

### How to Play

1. **Start Game** - Select "Play" from main menu
2. **Move Ship** - Use WASD or arrow keys to navigate
3. **Fire Bullets** - Press Space to shoot at enemies
4. **Destroy Enemies** - Each enemy destroyed adds points
5. **Survive** - Avoid enemy bullets to keep your lives
6. **Game Over** - Lose all lives or achieve win condition

### Game Mechanics

**Lives System:**
- Start with 3 lives
- Lose a life when hit by enemy bullet
- Game over when all lives are lost

**Scoring:**
- Enemy Level 1: 10 points per kill
- Enemy Level 2: 20 points per kill
- Enemy Level 3: 30 points per kill

**Difficulty Progression:**
- Enemy Level 1 appears at game start
- Enemy Level 2 spawns at score 100+
- Enemy Level 3 spawns at score 260+
- Enemies spawn more frequently as score increases

### Enemy Types

| Enemy Type | Health | Damage | Points |
|-----------|--------|--------|--------|
| **Level 1** | 1 HP | 10 damage | 10 pts |
| **Level 2** | 2 HP | 20 damage | 20 pts |
| **Level 3** | 3 HP | 30 damage | 30 pts |

---

## 🏗️ Architecture

### Class Hierarchy

**Entity (Base Class):**
- Shared attributes (position, speed, active state)

**Player:**
- Movement and controls
- Bullet firing mechanism
- Health management
- Collision handling

**Enemy (Abstract Base):**
- Virtual methods for polymorphism
- Enemy Level 1, 2, 3 implementations
- Unique damage and score values

**Bullet:**
- Projectile movement
- Collision detection
- Active/inactive state

**Button (UI):**
- Menu buttons
- Collision detection
- Event handling

---

## 📊 Game States

```
┌─────────────────┐
│   Main Menu     │
└────────┬────────┘
         │
    ┌────▼────┐
    │  Play   │
    └────┬────┘
         │
    ┌────▼────────────┐
    │  Game Playing    │
    └────┬────────────┘
         │
    ┌────▼────────────┐
    │  Game Over / Win │
    └─────────────────┘
```

---

## 💡 OOP Concepts Demonstrated

- **Inheritance** - Enemy hierarchy (base class → Level 1/2/3)
- **Polymorphism** - Virtual methods in Enemy class
- **Encapsulation** - Private data members with public methods
- **Composition** - Player contains Bullets
- **Abstraction** - Entity base class for common functionality

---

## 📈 Possible Enhancements

- [ ] Boss enemy waves
- [ ] Weapon upgrades and power-ups
- [ ] High score leaderboard
- [ ] Particle effects system
- [ ] Background music and sound effects
- [ ] Different game difficulty levels
- [ ] Multiplayer mode
- [ ] Achievement system

---

## 🎯 Gameplay Tips

- **Stay Mobile** - Keep moving to avoid enemy fire
- **Focus Fire** - Concentrate bullets on one enemy
- **Manage Health** - Prioritize survival over scoring
- **Pattern Recognition** - Learn enemy movement patterns
- **Watch Ammunition** - Keep firing for continuous damage

---

## 📜 License

This project is licensed under the **MIT License** - see [LICENSE](LICENSE) file for details.

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request

---

## 🎓 Learning Outcomes

This project demonstrates:
- ✅ Object-oriented programming principles
- ✅ Game loop implementation
- ✅ Collision detection systems
- ✅ Entity management
- ✅ State machine patterns
- ✅ Graphics rendering with Raylib
- ✅ Input handling and event processing
- ✅ Performance optimization

---

<div align="center">

**Created with ❤️ by Muhammad Hammad**

[⬆ back to top](#-space-shooter-game)

</div>
