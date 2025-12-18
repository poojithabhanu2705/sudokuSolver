🧩 Sudoku Solver (LeetCode 37)
📌 Problem Statement

Given a partially filled 9×9 Sudoku board, fill the empty cells (.) such that every row, every column, and each 3×3 subgrid contains the digits 1–9 exactly once.

The solution must modify the board in-place.

💡 Approach

This problem is solved using Backtracking, a depth-first search technique where we try all valid possibilities and undo choices when they lead to an invalid state.

Key Ideas

Traverse the board cell by cell

If a cell is already filled → move to the next cell

If a cell is empty:

Try digits '1' to '9'

Check if placing the digit is safe

Place the digit and recurse

If it fails → backtrack

🔐 Safety Check (isSafe)

Before placing a digit, ensure:

The digit is not present in the same row

The digit is not present in the same column

The digit is not present in the 3×3 subgrid

This guarantees Sudoku constraints are preserved.

🧠 Algorithm (Step-by-Step)

Start from the top-left cell (0,0)

Move row-wise across the board

For each empty cell:

Try digits 1–9

Validate using isSafe

Recurse to the next cell

If no digit fits, backtrack

Stop when all rows are processed (row == 9)

⏱️ Time & Space Complexity

Time Complexity:
Worst case: O(9^(number of empty cells))
(Highly optimized by pruning invalid states early)

Space Complexity:
O(1) extra space (excluding recursion stack, board modified in-place)
