# python-asteroids

Classic Asteroids arcade game built in Python with pygame. Fly a ship, shoot, and split incoming asteroids into smaller pieces.

## Requirements

- Python 3.13+
- [uv](https://docs.astral.sh/uv/)

## Getting started

```sh
uv sync
uv run main.py
```

## Controls

| Key     | Action          |
| ------- | --------------- |
| `W`     | Move forward    |
| `S`     | Move backward   |
| `A`     | Rotate left     |
| `D`     | Rotate right    |
| `Space` | Shoot           |

## Gameplay

- Asteroids spawn from the screen edges and drift across.
- Shooting a large asteroid splits it into two smaller ones; the smallest ones are destroyed outright.
- Colliding with an asteroid ends the game.

## Project structure

| File               | Purpose                                         |
| ------------------ | ----------------------------------------------- |
| `main.py`          | Game loop, sprite groups, collision handling    |
| `circleshape.py`   | Base class for circular sprites with collisions |
| `player.py`        | Player ship: movement, rotation, shooting       |
| `shot.py`          | Projectiles fired by the player                 |
| `asteroid.py`      | Asteroids and splitting logic                   |
| `asteroidfield.py` | Spawns asteroids at random screen edges         |
| `constants.py`     | Screen size, speeds, radii, cooldowns           |
| `logger.py`        | Writes game state/events to `*.jsonl` files     |

## Configuration

Tweak gameplay values (player speed, shot speed, shoot cooldown, asteroid spawn rate, etc.) in `constants.py`.
