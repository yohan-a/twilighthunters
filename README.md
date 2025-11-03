# Twilight Hunters

A fast-paced 2D top-down shooter built with Pygame. Battle waves of ghouls, ghosts, and skeletons in a TMX tile-mapped world with pixel-perfect collisions, responsive controls, and punchy audio.
**Runs on Windows, macOS, and Linux—launch from the main menu and play with keyboard + mouse.**

## Table of Contents

- [Project Overview](#project-overview)
- [Software Requirements](#software-requirements)
- [Installation](#installation)
- [Features](#features)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Troubleshooting](#troubleshooting)
- [Credits](#credits)

## Project Overview

Twilight Hunters is a Python/Pygame top-down shooter featuring a main menu, credits, game loop, enemy spawns, bullet collisions, and a tilemap-based world loaded via PyTMX. It uses mask-based collision for precise hits and a simple audio system for music and SFX.

## Software Requirements

- Python 3.x
- Dependencies listed in `requirements.txt` (`pygame`, `pytmx`)

## Installation

1. **Clone the repository**
  git clone https://github.com/yohan-a/twilighthunters
  cd twilighthunters
  
2. **Install dependencies**
  pip install -r requirements.txt

3. **Run from the main menu**
  python code/mainmenu.py

## Features

- Main Menu: START, CREDITS, QUIT; requires a background image `bg.png`
- Player movement: 4-directional animations with normalized input
- Gun system: cooldown-based firing with bullet spawn offset
- Enemies: timed spawns and pursuit behavior; pixel-perfect mask collisions
- Collisions: accurate bullet-vs-enemy detection using mask collisions
- Audio: looping background music, shooting and impact SFX (WAV/OGG)
- World: TMX tilemap loading (e.g., `data/maps/world.tmx`)
- Game Over: dedicated screen; ESC exits the session

## Usage

- Launch the main menu and click START to play.
- **Controls:**
- Movement: WASD or Arrow Keys
- Aim: Mouse cursor
- Shoot: Left Mouse Button
- Quit: ESC on the Game Over screen
- Ensure assets exist in `images/` and `audio/`, and the world map is at `data/maps/world.tmx`

## Project Structure

```
twilighthunters/
├── README.md                   # Project documentation
├── requirements.txt            # Python dependencies (pygame, pytmx)
├── bg.png                     # Background image used in main menu
├── audio/                     # Audio assets (music, SFX)
├── code/                      # Source code files
│   ├── main.py
│   ├── mainmenu.py
│   ├── player.py
│   ├── sprites.py
│   ├── groups.py
│   ├── settings.py
│   └── gameover.py
├── data/                      # Game data files
│   ├── maps/                 # TMX tilemap files
│   └── tilesets/             # Tileset assets referenced in TMX maps
└── images/                    # All image assets
    ├── player/               # Player animations
    ├── enemies/              # Enemy animations
    └── gun/                  # Gun and bullet sprites
```

## Troubleshooting

- Missing dependencies: use `pip install -r requirements.txt` in the active environment
- Asset paths: run from the repo root so `images/`, `audio/`, and `data/maps/` resolve correctly
- Audio errors: ensure `audio/music.wav`, `audio/shoot.wav`, and `audio/impact.ogg` exist
- Menu background: add `bg.png` where `mainmenu.py` expects it or update the path
- TMX map: verify `data/maps/world.tmx` exists and tilesets resolve

## Credits

Developed by Yohan Amaratunga, Fatema Ahmed, Tomoghna Mitra, and Maani Rezaei.
