# Knight's Travails

This is a solution to the Knight's Travails problem: given a grid the size of a chess board, determine the shortest possible path between a starting position and ending position for a knight piece.

## My Solution Explained

My solution uses a Tree structure to determine the shortest path. Here's the general algorithm:

1. For each position on the chess board, create a corresponding Tree node.
2. Build up a move tree for each potential pathway. This tree is limited by the fact that you don't return to any square.
3. Run a breadth-first search on the move tree, with the root being the tree node corresponding to the starting square and the target being the node corresponding to the target square. 
4. If a solution path is found, build up a path array by tracing the parent nodes from the ending position to the starting position.

## Project Notes

* The tree node data structure is factored out into it's own class, so it can be reused for other purposes.
* The treenode.rb file is used solely for the purposes of testing/debugging.