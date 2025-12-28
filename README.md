# Squares

---

## About

**Squares** is a puzzle game that takes some time to learn, but not too much. Once you've learned it, it starts very easy and quickly gets very hard.

It's not for everybody, but maybe it's for you.

**Google Form for anonymous feedback: [Submit feedback](https://docs.google.com/forms/d/e/1FAIpQLSeIaxNyCdi28-s6i97ejHl93_0c3DgvRkqi4oMgkQ-syXueDA/viewform?usp=sf_link)**

---

## FAQ

### I chose "difficult" and the board that came out was easy. What happened?

The difficulty buttons set parameters (color frequency, board size, maximum number of solutions) and then generate a random board based on these. You should never get a difficult board if you select "easy," but you might randomly get a relatively easy board if you select "difficult." There isn't a good way (yet) to automatically determine whether a board is difficult.

### I chose some settings and asked for a new board and the app crashed. What happened?

This can happen with certain combinations of settings (e.g., lots of difficult colors, large board size) when either or both of these things happen:

- The game can't find a board with the specified number of solutions. Usually, larger boards have more solutions.
- The game can't find a solvable board. Some configurations of colors are unsolvable since they lead to loops that can't be resolved.

The game tries random board after board to find one that works, and it may "crash" as it keeps looking for one. I will implement a fix for this, but for now if this happens go to [https://squaresga.me/?0](https://squaresga.me/?0) and you can change your settings. This should never happen with one of the difficulty buttons.

### The game has the wrong solution for a board.

Please share it at the feedback link above. You can just copy and paste the URL, making sure to include the digits after the question mark. I've tried to eliminate any bugs in the solving algorithm, but it's always possible that I've missed some.

### I created a board and it says there are 0 solutions.

There are two possibilities:

1. **No solutions exist**: Every square touches more red than green. For example, a board of all red squares would have this issue, but it might occur in many boards.

2. **Unsolvable due to circularity or irreconcilable paths**: The board has logical conflicts that prevent solutions. For example:
   - Two squares that each cancel the other, creating a paradox where both can't be canceled simultaneously, and there's no rule to choose precedence.
   - Circular logic where a chain of squares creates an endless loop of extending and retracting.

You will never have this problem with daily boards or with the New button, since boards with 0 solutions or that are unsolvable are thrown out. But you may encounter it when making your own board.

---

## Play the Game

Visit [https://squaresga.me](https://squaresga.me) to play!
