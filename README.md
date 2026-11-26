# ⭕❌ Tic Tac Toe

A two-player Tic Tac Toe game built with vanilla HTML, CSS and JavaScript. Take turns on a shared board, get an instant winner announcement, and start a fresh game with one click. No frameworks, no build step, no dependencies.

**[Play it live](https://YOUR-USERNAME.github.io/tic-tac-toe/)** <!-- replace after enabling GitHub Pages -->

<!-- Add a screenshot: save it as screenshot.png in the repo and uncomment the line below -->
<!-- ![Tic Tac Toe screenshot](screenshot.png) -->

---

## ✨ Features

- Two-player, same-device gameplay (O goes first, then X)
- Automatic win detection across all 8 winning lines (3 rows, 3 columns, 2 diagonals)
- Winner announcement banner with a **New Game** button
- **Reset Game** button available at any time
- Filled squares are locked, and the whole board locks once someone wins
- Responsive board sized with `vmin` units, so it scales on phones and desktops
- Zero setup: open `index.html` and play

## 🎮 How to Play

1. Player **O** starts. Click any empty square to place your mark.
2. Players alternate turns, with **X** going next.
3. Get three of your marks in a row, column or diagonal to win.
4. When someone wins, a banner announces the winner. Click **New Game** (or **Reset Game**) to play again.

## 🛠️ Built With

- **HTML5** for the page structure
- **CSS3** (Flexbox, `vmin` units) for the responsive layout
- **Vanilla JavaScript (ES6+)** for turn handling and win detection

## 📁 Project Structure

```
tic-tac-toe/
├── index.html   # Board markup and buttons
├── style.css    # Layout and styling
├── app.js       # Turn logic, win detection, reset
└── README.md
```

## 🚀 Getting Started

### Run locally

```bash
# 1. Clone the repository
git clone https://github.com/YOUR-USERNAME/tic-tac-toe.git

# 2. Move into the folder
cd tic-tac-toe

# 3. Open index.html in your browser
```

You can also double-click `index.html`, or use any local server:

```bash
# Python
python -m http.server 8000

# Node
npx serve
```

### Deploy with GitHub Pages

1. Push the project to a GitHub repository.
2. Go to **Settings → Pages**.
3. Under **Source**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
4. Save. Your game will be live at `https://YOUR-USERNAME.github.io/tic-tac-toe/` within a minute or two.

## 🧠 How It Works

- The board is nine `<button class="box">` elements. Clicking one writes the current player's mark into it and disables it.
- A boolean (`turn0`) tracks whose turn it is and flips after every move.
- `winpattern` holds the eight winning index combinations. After each move, `checkWinner()` checks whether all three squares in any pattern match and are non-empty.
- On a win, `showWinner()` displays the banner and disables the rest of the board.
- `resetgame()` clears the squares, re-enables them, hides the banner and gives O the first move again.

## 🗺️ Roadmap

- [ ] Detect and announce a draw when the board fills up with no winner
- [ ] Show whose turn it is
- [ ] Add a score tracker across multiple rounds
- [ ] Highlight the winning line
- [ ] Single-player mode against the computer
- [ ] Let players choose who goes first
- [ ] Dark mode

## 🤝 Contributing

Contributions, issues and feature requests are welcome.

1. Fork the project
2. Create your feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m "Add my feature"`
4. Push to the branch: `git push origin feature/my-feature`
5. Open a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE). <!-- add a LICENSE file, or remove this section -->

---

Made with ❤️ by [YOUR NAME](https://github.com/YOUR-USERNAME)
