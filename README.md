# Artificial-Intelligence
Goal of Project: Given images of Sudoku Puzzles, solve Sudoku.

Work Distribution:
Bhanu -- Creating convolutional neural networks two extract Sudoku puzzles from images.
Nate -- Solveing Sudoku puzzles in an extremly quick manner.

Datasets used (See presentation/paper for hyperlinks): 
Kaggle: Sudoku Box Detection
Kaggle: Digits

Notes on Sudoku solving:
Sudoku was solved using a recursive depth-first method.  The cell chosen for each branch is determined by the most constraining hueristic. The idea behind this is that the more possible values are removed, the less branchs to search later on.  At each stage of the search, the oneRun function is performed multiple times to place number in the cells with only one possible value.  The function also simultaneously checks for a solved Sudoku.  This allows the Sudoku to solve itself instantanouesly when it is close to a solution.  If the Sudoku is not solved at a particulat point, a consistency-check is performed to ensure that the current branch leads to possible soltions.  All of these methods combined prune enough branch to get near-instantaneous Sudoku results.
