# 8-Puzzle Solver (Misplaced Tiles Heuristic)

## Overview
This C++ program solves the classic **8-puzzle problem** using the **Misplaced Tiles heuristic**.  
It applies a **Best-First Search** approach, selecting the next state with the fewest misplaced tiles compared to the goal state.

The goal configuration is:

1 2 3
4 5 6
7 8 0

yaml
Copy
Edit
Where `0` represents the blank tile.

---

## Features
- **User input** for the initial puzzle state.
- Uses **Misplaced Tiles heuristic** to guide search.
- Displays the **step-by-step solution** from start state to goal state.
- Detects if no solution exists.

---

## How the Algorithm Works
1. **Heuristic Function**: Counts the number of tiles out of place (excluding the blank).
2. **Priority Queue**: Expands the puzzle states with the smallest heuristic value first.
3. **Path Tracking**: Stores the sequence of states from start to goal.
4. **Move Generation**: Swaps the blank tile up, down, left, or right to create new states.
5. Stops when:
   - The goal state is reached.
   - All possible states are explored without finding the goal.

---

## Example Input & Output

**Input**
Enter puzzle (0 for blank):
1 2 3
4 0 6
7 5 8


**Output**
--- Solution Found (Misplaced Tiles) ---
1 2 3
4 0 6
7 5 8
1 2 3
4 5 6
7 0 8
1 2 3
4 5 6
7 8 0

---

# Use Case
This program can be used for:

AI learning: Demonstrates heuristic-based search.

Educational purposes: Understanding the 8-puzzle and search algorithms.

Algorithm comparison: Can be extended to use other heuristics like Manhattan Distance.

## Usage
1. Compile the program:
   ```bash
   g++ puzzle_solver.cpp -o puzzle_solver
Run the program:

  ```bash
     ./puzzle_solver

