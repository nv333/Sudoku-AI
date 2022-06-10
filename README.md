# Sudoku-AI
AI Sudoku solving algorithm

## Algorithmic Approach: 
Constraint propagation is a suitable algorithmic choice when modelling Sudoku puzzles as a constraint satisfaction problem. To decide which numbers are assigned to the cells, the set of constraints must be satisfied, which dictates no number may be repeated in any row, column or square (3x3) in the grid. Once this has been satisfied, the solution has been found.

By including backtracking, the solver also searches for consistent number assignments, rather than solely focusing on eliminating inconsistent ones, which is more efficient. It does this by fully exploring each possible assignment to every cell until an inconsistent one is made, causing it to backtrack to a previous consistent state and continue, or a solution is found.

Dynamic variable ordering increases efficiency by making the informed decision of which cell to assign to next. For this, Most Constrained Variable and Degree heuristics were used. The former works by pruning branches for inconsistent assignments sooner, and the latter acts as a tie-breaker if needed, choosing the cell which, if assigned to, would affect the largest number of cells.

For future updates, some form of visualisation could be attempted which could show the path the solver takes within the depth-first search, or perhaps which values in the solved cell required most backtracking using a heat-map for demonstration.
