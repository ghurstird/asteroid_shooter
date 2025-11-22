# Asteroid Game

A classic Asteroids arcade-style game built with Python and Pygame. Navigate your spaceship through waves of asteroids, shooting them down before they collide with you!

## Features

- **Classic Gameplay**: Experience the timeless arcade action of the original Asteroids game
- **Player Controls**: Rotate your ship, thrust forward, and fire shots at asteroids
- **Dynamic Asteroids**: Asteroids spawn continuously and break into smaller pieces when destroyed
- **Collision Detection**: Circle-based collision detection for accurate gameplay
- **Game Logging**: Event and state logging for debugging and analytics
- **Responsive Controls**: Smooth keyboard-based ship controls with precise aiming

## Requirements

- Python 3.12+
- Pygame 2.6.1

## Installation

1. Clone the repository:
```bash
git clone https://github.com/ghurstird/asteroid_game.git
cd asteroid_game
```

2. Install dependencies using pip:
```bash
pip install -r requirements.txt
```

Or using uv (if available):
```bash
uv sync
```

## Running the Game

Start the game by running:
```bash
python main.py
```

## Controls

- **Arrow Keys** or **A/D**: Rotate your spaceship left/right
- **W** or **Up Arrow**: Thrust forward
- **Space**: Fire shots at asteroids

## Game Mechanics

- **Player Ship**: A triangular spaceship that can rotate and move across the screen
- **Asteroids**: Circular asteroids of varying sizes spawn continuously at the edges of the screen
- **Shots**: Fire projectiles to destroy asteroids
  - Each asteroid destroyed splits into 2 smaller asteroids (up to 3 levels)
  - Smallest asteroids are destroyed completely
- **Game Over**: Touching an asteroid ends the game

## Project Structure

- `main.py` - Main game loop and event handling
- `player.py` - Player spaceship class with movement and shooting logic
- `asteroid.py` - Asteroid class with collision and splitting behavior
- `asteroidfield.py` - Manages asteroid spawning and waves
- `shot.py` - Projectile class
- `circleshape.py` - Base class for circular collision objects
- `constants.py` - Game configuration constants (speeds, sizes, etc.)
- `logger.py` - Event and state logging utilities
- `game_events.jsonl` - Log of in-game events
- `game_state.jsonl` - Log of game state snapshots

## Configuration

Edit `constants.py` to adjust game parameters:

```python
SCREEN_WIDTH = 1280          # Game window width
SCREEN_HEIGHT = 720          # Game window height
PLAYER_RADIUS = 20           # Player ship size
PLAYER_TURN_SPEED = 300      # Rotation speed (degrees/sec)
PLAYER_SPEED = 200           # Thrust speed (pixels/sec)
ASTEROID_MIN_RADIUS = 20     # Smallest asteroid size
ASTEROID_SPAWN_RATE_SECONDS = 0.8  # Time between spawns
PLAYER_SHOT_SPEED = 500      # Projectile speed
PLAYER_SHOOT_COOLDOWN_SECONDS = 0.3  # Time between shots
```

## Development

The project uses a modular sprite-based architecture with:
- **Sprite Groups** for managing updatable and drawable objects
- **Delta Time** for frame-rate independent movement
- **Collision Detection** using circle-based physics
- **Event Logging** for game analytics and debugging

## Future Enhancements

- Score tracking and high scores
- Sound effects and background music
- Power-ups and special weapons
- Multiple difficulty levels
- Enemy spaceships
- Particle effects for explosions
