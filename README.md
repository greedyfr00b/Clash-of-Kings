# Clash of Kings — Browser Card Game

A mobile-friendly, single-file web game where you play **Clash of Kings** against up to three AIs. Optimized UI, clear rules, and a tougher *Hard* AI that prioritizes high-ending runs.

> Play locally by opening `index.html` in your browser, or deploy to GitHub Pages with the workflow below.

## Features
- Responsive UI tailored for phones and desktops
- 2–4 players (You + up to 3 AIs), with **Easy / Normal / Hard** difficulties
- Smart AI on *Hard*: prefers the **highest-ending run**, then length, to keep pressure on
- Priority-view hand ordering during a move so playable cards bubble to the front
- Auto-draw until you have something playable (with safeguards for forced Ace rules)

## Game Rules (Quick)
- Two piles: **Left** (♠/♥) and **Right** (♣/♦).
- On your turn, choose a pile and play:
  - The first card must be the **opposite suit** of the pile’s top, and **rank ≥** the top.
  - Subsequent cards must strictly **alternate suits** and **increment rank by 1**.
- **Aces** are special: you may place an Ace on its matching side (♠/♥ or ♣/♦) regardless of the previous suit. **Only an Ace** finishes a pile; finished piles reopen as empty for the next player.
- Drawing: You can draw (auto-draws) **only if you have no playable non-Ace** and you’re not exceeding the Ace limit.
- Win by emptying your hand first.

## Controls
- **Start**: begin a new game with current settings.
- **Draw**: auto-draw until you can play (or deck runs out / Ace forced).
- **Finish**: commits the staged play(s) to the chosen pile.
- **Reset**: clears staged cards.
- **Pass**: if nothing can be done and the deck is empty.

## Local Run
Just open `index.html` in any modern browser. No build step required.

## GitHub Pages Deploy
This repo includes a Pages workflow. To publish:
1. Create a new GitHub repository and upload these files.
2. Go to **Settings → Pages → Build and deployment → Source** and select **GitHub Actions**.
3. Push to `main`. The `Deploy static site to Pages` workflow publishes to `https://<your-username>.github.io/<repo-name>/`.

> If you use a custom domain, add a `CNAME` file in the repo root containing your domain name.

## Contributing
Bug reports and feature requests are welcome! See **CONTRIBUTING.md** and our **Code of Conduct**.

## License
MIT © 2025 Chandler
