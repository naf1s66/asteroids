# Asteroids Game

A Python implementation of the classic Asteroids arcade game using Pygame. Navigate your spaceship through an asteroid field, shoot asteroids to break them into smaller pieces, and survive as long as possible!

## Features

- **Classic Gameplay**: Control a triangular spaceship in a 2D space environment
- **Asteroid Physics**: Asteroids split into smaller fragments when shot, creating dynamic gameplay
- **Smooth Controls**: WASD movement with space bar shooting
- **Game State Logging**: Automatic logging of game state and events to JSONL files for analysis
- **Collision Detection**: Precise circular collision detection for player, asteroids, and shots

## Controls

- `W` - Move forward
- `A` - Rotate left
- `D` - Rotate right
- `S` - Move backward
- `Space` - Shoot

## Requirements

- Python 3.13+
- Pygame

## Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd asteroids

# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install pygame
```

## Running the Game

```bash
python main.py
```

## Game Mechanics

- **Player**: Triangle-shaped ship with rotation and movement controls
- **Asteroids**: Spawn periodically at screen edges, moving in random directions
- **Shooting**: Fire projectiles with a cooldown of 0.3 seconds
- **Splitting**: Asteroids break into two smaller asteroids when hit (until minimum size)
- **Game Over**: Collision with any asteroid ends the game

## Project Structure

- `main.py` - Main game loop and initialization
- `player.py` - Player ship class with controls
- `asteroid.py` - Asteroid entities and split mechanics
- `shot.py` - Projectile class
- `circleshape.py` - Base class for circular collision detection
- `asteroidfield.py` - Asteroid spawning system
- `constants.py` - Game configuration and constants
- `logger.py` - Game state and event logging system

## Logging

The game automatically logs:
- **Game State** (`game_state.jsonl`): Sprite positions, velocities, and counts every second
- **Game Events** (`game_events.jsonl`): Player hits, asteroid splits, and shots fired

Perfect for analyzing gameplay patterns or creating AI training data!
