# N-Puzzle Problem: Solving with A* and DFS

## Introduction
The **n-puzzle** is a classical problem in the field of artificial intelligence and search algorithms. It involves an \( N \times N \) grid where one tile is missing, and the goal is to rearrange the tiles to a target configuration by sliding the tiles around. The puzzle has many variations, such as the **8-puzzle** (3x3 grid) and the **15-puzzle** (4x4 grid). The problem is often used to model and test search algorithms that incorporate heuristics for finding optimal or near-optimal solutions.

## Solutions

### 1. **A* Search**
The **A* search algorithm** is an informed search algorithm that uses a combination of two factors to prioritize the most promising states to explore:
- **g-score**: The cost of reaching the current state from the start.
- **h-score**: A heuristic estimate of the cost from the current state to the goal.

A* uses the **f-score**, calculated as \( f = g + h \), to determine which states to expand first, with the lowest f-score having the highest priority.

**Heuristics used in A* for the n-puzzle**:
- **Misplaced Tiles**: Counts the number of tiles that are not in their correct positions in the goal configuration.
- **Manhattan Distance**: The sum of the vertical and horizontal distances of each tile from its target position.



### 2. **Depth-First Search (DFS)**
**DFS** is an uninformed search algorithm that explores as deep as possible along each branch before backtracking. It uses a stack data structure (either explicit or via recursion) to manage the nodes to visit.

DFS does not guarantee an optimal solution and may take longer to find a solution in larger puzzles. While it uses less memory compared to A*, it can suffer from performance issues in high-dimensional problems due to deep branching.


## Conclusions
- **A*** is highly effective for smaller puzzles such as the **8-puzzle**, providing optimal solutions in a reasonable time. However, it becomes computationally infeasible for larger puzzles like the **15-puzzle** due to the large search space and high memory consumption.
  
- **DFS** is less memory-intensive and may provide solutions for smaller problems, but it is inefficient and often impractical for larger puzzles. It does not guarantee optimality and can take excessive time due to its deep branching nature.

In conclusion, **A*** with an admissible heuristic such as Manhattan Distance or Misplaced Tiles is generally preferred for solving the n-puzzle when optimal solutions are needed. However, for larger puzzles or when time constraints are strict, more efficient heuristics or alternative algorithms may be required.
