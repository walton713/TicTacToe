# TicTacToe

Can you write a simple check for the status of a tic-tac-toe board?

## Requirements

---

Write a public api to get the status of a tic-tac-toe board

* The public api should consist of a single public function that takes in a 2D array of integers and returns an integer
* The status of each board space is described as follows:
  * 0 - the space is empty
  * 1 - the space is occupied by an X
  * 2 - the space is occupied by an O
* The status of the board itself should be described as follows:
  * -1 - the game is unfinished
  *  0 - the game is a cat's game (nobody one)
  *  1 - the game is won by X
  *  2 - the game is won by O

The rules for tic-tac-toe can be found here: [Tic-Tac-Toe Rules](https://en.wikipedia.org/wiki/Tic-tac-toe)

## Assumptions

---

1. The board represented by the 2D array is valid in the context of a 3x3 game of tic-tac-toe

## Features

---

## Unfinished Game

_As a tic-tac-toe player <br />
I want to know that the game is unfished <br />
So that I know to keep playing_

A game is unfinished if no one has won yet and there are still open spaces on the board.

### Example

```
[[ 2, 2, 0 ],
 [ 2, 0, 1 ],
 [ 0, 1, 2 ]]
```

### Scenarios

_Given a tic-tac-toe board <br />
When there are open spaces <br />
And no one has won <br />
Then the game is unfinished_

---

## Player Wins

_As a tic-tac-toe player <br />
I want to know a player has won the game <br />
So that I know the game is over_

A game is won when one of the players gets three spaces in a row, either horizontally, vertically or diagonally.

### Example

```
[[ 1, 2, 0 ],
 [ 2, 1, 0 ],
 [ 2, 1, 1 ]]
```

### Scenarios

_Given a tic-tac-toe board <br />
When there are 3 X's in a row <br />
Then X wins_

_Given a tic-tac-toe board <br />
When there are 3 O's in a row <br />
Then O wins_

---

## Cat's Game

_As a tic-tac-toe player <br />
I want to know the game is a cat's game <br />
So that I know the game is over_

A game is considered a cat's game when there are no more spaces open and a player has not gotten three spaces in a row.

### Example

```
[[ 1, 2, 2 ],
 [ 2, 1, 1 ], 
 [ 2, 1, 2 ]]
```

### Scenarios

_Given a tic-tac-toe board <br />
When there are no empty spaces <br />
And no one has won <br />
Then the game is a cat's game_
