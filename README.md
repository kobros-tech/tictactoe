# Tic-Tac-Toe AI

A browser-based Tic-Tac-Toe game where you play against an unbeatable AI powered by the **Minimax algorithm** with **Alpha-Beta Pruning**.

🎮 **[Play it live](https://tictactoe.kobros-tech.com)**

---

## How it works

The AI doesn't learn or guess — it thinks. Before every move, it simulates every possible future game, assumes you also play perfectly, and picks the move that guarantees the best outcome for itself. This is called the **Minimax strategy**.

**Alpha-Beta Pruning** is layered on top as an optimization: it skips branches of the game tree that can't possibly influence the final decision, making the search significantly faster without changing the result.

The outcome: the AI is mathematically unbeatable. The best you can achieve is a **draw** — but only if you play perfectly too.

---

## Features

- Play as **X** (go first) or **O** (go second)
- AI responds instantly using client-side Minimax
- Winning line highlighted at end of game
- Score tracker across multiple rounds
- Hover preview shows where your mark will go
- Fully responsive — works on desktop and mobile

---

## Tech stack

- Pure **HTML, CSS, and JavaScript** — no frameworks, no dependencies
- AI logic runs entirely in the browser
- Hosted on **GitHub Pages** with a custom domain

---

## Run locally

No build step needed. Just clone and open:

```bash
git clone https://github.com/yourusername/tictactoe.git
cd tictactoe
open index.html
```

Or simply drag `index.html` into any browser.

---

## The algorithm

```
minimax(board):
  if terminal(board):
      return utility(board)        # +1 X wins, -1 O wins, 0 draw

  if current player is X:
      return max over all actions of minimax(result(board, action))
  else:
      return min over all actions of minimax(result(board, action))
```

Alpha-Beta Pruning improves this by tracking the best already-found options for each player (`alpha` for X, `beta` for O) and cutting off any branch where further search can't improve the result.

---

## Project structure

```
tictactoe/
└── index.html      # Game UI + embedded AI logic
└── README.md
```

---

## License

MIT — free to use, modify, and share.
