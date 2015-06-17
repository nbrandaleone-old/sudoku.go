# sudoku.go
Solves "easy" (fully constrained) sudoku problems using Go computer language.

This is one of my favorite Go programs.

There are 81 go routines running, one for each cell or square in the board.
They listen to messages for given values, thereby eliminating possible number choices. 
Once all but one choice is eliminated, the routines know that they MUST
be the remaining choice. They send this answer on a new solution channel.
When all the solutions are collated, the answer is printed out.
