# 🤖 Warehouse Robot Path Planner — A*

An interactive browser-based implementation of **A\* pathfinding** for a warehouse robot moving through a grid.

## Features

- A* shortest-path algorithm
- Manhattan-distance heuristic
- Priority queue / min-heap concept
- 10 × 15 warehouse grid
- Obstacles
- Animated node exploration
- Animated shortest path
- Distance, nodes explored and execution time
- No-path detection
- Add obstacles with left click
- Remove obstacles with right click
- Reset button
- Works directly in a web browser

## Algorithm

The project uses A*:

**f(n) = g(n) + h(n)**

Where:
- `g(n)` = actual cost from the start
- `h(n)` = estimated remaining cost
- Manhattan distance: `|x1-x2| + |y1-y2|`

The robot moves only horizontally and vertically, so Manhattan distance is used.

## How to run

Open `index.html` in a browser.

For GitHub Pages, upload this repository to GitHub and enable:

**Settings → Pages → Deploy from branch → main → / (root)**

GitHub will provide a public URL such as:

`https://YOUR-USERNAME.github.io/warehouse-robot-astar/`

## Controls

- Left click: add obstacle
- Right click: remove obstacle
- FIND SHORTEST PATH: run A*
- RESET: restore the original warehouse

## Project Questions

### Which algorithm did you use?
We use the A* pathfinding algorithm.

### Why A*?
A* efficiently finds a shortest path by combining the actual cost from the starting node with a heuristic estimate of the remaining distance.

### What data structure did you use?
The original Python implementation uses Python's `heapq` priority queue. In this browser implementation, an ordered open list is used to reproduce the same lowest-cost-node selection.

### What is your heuristic?
Manhattan distance:

`h(n) = |x1 - x2| + |y1 - y2|`

### What is an obstacle?
An obstacle represents a blocked warehouse location that the robot cannot enter.

### What happens if there is no path?
The algorithm explores all reachable cells and reports that no feasible path exists.
