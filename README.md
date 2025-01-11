Here is a sample `README.md` for your Room Cleaning Agent code:

---

# Room Cleaning Agent

This project implements a simple Reflex Agent that simulates cleaning a room represented as a 2D grid. The agent perceives the cleanliness of its current position, performs actions (cleaning if dirty), and moves to optimize the cleaning process.

## Features

- **Randomized Room State**: The room is initialized as a 10x10 grid with cells randomly marked as clean (`0`) or dirty (`1`).
- **Agent Behavior**:
  - Starts at a random position in the grid.
  - Cleans dirty cells.
  - Moves intelligently to unvisited and dirty cells to optimize cleaning.
- **Interactive Display**:
  - Shows the initial room status.
  - Tracks each cleaning step.
  - Displays the final cleaned room status and the number of steps taken.

## How It Works

1. **Initialization**: 
   - A `10x10` grid room is generated with random cell states (`0` for clean, `1` for dirty).
   - The agent is placed at a random position in the grid.

2. **Perception and Action**:
   - The agent checks if its current cell is dirty.
   - If dirty, the cell is cleaned by setting its value to `0`.

3. **Optimized Movement**:
   - The agent prioritizes unvisited dirty cells in its immediate neighborhood.
   - If no dirty cells are nearby, it moves to any unvisited cell.
   - If all cells are visited but some remain dirty, it moves to the nearest dirty cell.

4. **Termination**:
   - The agent stops when the entire room is clean.

## Code Structure

- **`ReflexAgent` Class**:
  - `__init__(room_size)`: Initializes the room and agent's starting position.
  - `display_room()`: Displays the room's current state.
  - `perceive()`: Checks the cleanliness of the current cell.
  - `act()`: Cleans the cell if dirty.
  - `optimized_move()`: Determines the agent's next move based on room state.
  - `is_room_clean()`: Checks if all cells in the room are clean.
  - `run()`: Executes the cleaning process and displays the results.

## How to Run

1. Ensure you have Python installed on your system.
2. Copy the code into a file named `room_cleaning_agent.py`.
3. Run the file:
   ```bash
   python room_cleaning_agent.py
   ```
