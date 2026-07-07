# 🚀 Space Explorer

A Scratch arcade game built as part of **CS50's Introduction to Computer Science (CS50x)** — Problem Set 0: Scratch.

## Overview

Space Explorer is a catch-and-avoid arcade game. You pilot a rocketship along the bottom of the screen, catching falling stars for points while dodging falling balls that cost you lives. The game ends when you run out of lives.

## How to Play

- Move the rocketship **left** and **right** using the **arrow keys**.
- The rocketship is confined to the screen — it cannot move past the left or right edges.
- **Stars** fall from random positions at the top of the screen.
  - Catching a star with the rocketship adds **1 point** to your `Score` and respawns the star at a new random position.
- **Balls** also fall from random positions at the top of the screen.
  - Touching a ball with the rocketship removes **1 life** from your `Lives` counter and respawns the ball.
- You start with **3 lives**.
- When `Lives` reaches **0**, the rocketship displays "**Game Over!**" for 2 seconds and the game stops.

## Game Logic

- **Rocketship**: Controlled via `key pressed?` checks on the left/right arrow keys, using `change x by` to move and `set x` to clamp position at the screen edges. A custom block initializes `Score`, `Lives`, and the rocketship's starting position when the green flag is clicked.
- **Star / Ball**: Each uses a loop that repositions the object at a random x-coordinate at the top of the stage, then falls via `change y by` until it either touches the Rocketship (triggering a score/life change and respawn) or passes off the bottom of the screen, at which point the fall cycle restarts.

## Sprites & Assets

| Sprite | Role |
|---|---|
| Rocketship | Player-controlled character |
| Star | Collectible — increases score |
| Ball | Obstacle — decreases lives |
| Stage | Starfield backdrop |

## Built With

- [Scratch 3.0](https://scratch.mit.edu/) (MIT Media Lab)

## Course Context

This project was completed as part of **CS50x: Introduction to Computer Science**, offered by **Harvard University**. Problem Set 0 introduces fundamental programming concepts — variables, conditionals, loops, and events — using Scratch's visual block-based environment before transitioning to text-based languages later in the course.

## Author

Built by Kutty as part of ongoing CS50x coursework.

## Acknowledgements

- [CS50x](https://cs50.harvard.edu/x/) — Harvard University's Introduction to Computer Science
- [Scratch](https://scratch.mit.edu/) — MIT Media Lab
