# Marxian Competitive Dynamics Simulator

An interactive model of the competitive mechanism described in Marx's *Capital*, Volumes I and III — specifically how technology investment displaces living labor, drives down unit cost of production, and generates market advantage, while simultaneously raising the organic composition of capital and suppressing the rate of profit.

**[Live demo →](https://sswamy2000.github.io/marx-simulator/marx-simulator-v2.html)**

**[Technical documentation (PDF) →](https://sswamy2000.github.io/marx-simulator/marx-simulator-docs.pdf)**

---

## What it models

Marx argues in Vol. I (Ch. 15) and Vol. III (Ch. 13–15) that individual firms adopt labor-saving machinery to undercut competitors on price. This tool lets you simulate that dynamic directly.

Output is grounded in actual production inputs — all four factors multiply together:

```
output = workers × hours/day × days/week × 52 × tech multiplier
```

Each labor-hour produces one widget at a tech multiplier of 1. Both firms are price takers. Market share is proportional to each firm's actual output. A firm whose cost per widget exceeds the market price cannot cover costs and exits production.

---

## Key concepts

| Symbol | Marx's term | What it means |
|--------|-------------|---------------|
| `v` | Variable capital | Annual living labor (hours index) — the source of surplus value |
| `C` | Constant capital | Total capital stock (machinery, fixed assets) — transfers value, creates none |
| `s` | Surplus value | Revenue minus total annual cost — appropriated from living labor |
| `C/v` | Organic composition | Rising ratio signals capital deepening and labor displacement |
| `s/(C+v)` | Rate of profit | Tends to fall as C rises relative to v — the Vol. III formulation |

---

## Key inputs

- **Workers** — sets production scale; does not affect cost per widget
- **Hours per day** — physiological warnings above 10 hrs (amber) and 12 hrs (red)
- **Days per week** — combined with hours/day determines weekly labor burden
- **Tech multiplier** — the only input that lowers cost per widget; primary competitive variable
- **Capital lifespan** — longer lifespan inflates C, suppressing rate of profit without affecting cost/unit
- **Market price** — exogenous to both firms; drag it down to simulate competitive price destruction
- **Market size** — fixed inelastic demand; combined output exceeding this triggers unsold widget costs

---

## Features

- All inputs have both a slider and a direct number entry field, synchronized
- Physiological labor warnings at 50+ and 60+ weekly hours
- Market exit flag when cost/unit exceeds market price
- Unsold widget cost tracking when total supply exceeds market size
- One-click Excel export via SheetJS — captures all inputs and outputs, fully formatted
- Dark mode support

---

## Usage

Single self-contained HTML file. No build step, no dependencies, no framework required.

```bash
git clone https://github.com/sswamy2000/marx-simulator
cd marx-simulator
open marx-simulator-v2.html
```

Or open `marx-simulator-v2.html` directly in any browser.

---

## Deploy to GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Live at `https://sswamy2000.github.io/marx-simulator`

---

## Source texts

- Marx, K. *Capital: A Critique of Political Economy, Vol. I* — Part IV, Ch. 15: Machinery and Large-Scale Industry; Ch. 10: The Working Day
- Marx, K. *Capital: A Critique of Political Economy, Vol. III* — Part III, Ch. 13–15: The Law of the Tendency of the Rate of Profit to Fall
- Harvey, D. *The Limits to Capital* (1982)
- Shaikh, A. *Capitalism: Competition, Conflict, Crises* (2016)

---

## Author

Steven Swamy — [github.com/sswamy2000](https://github.com/sswamy2000)

---

## License

MIT License — © 2025 Steven Swamy

Permission is hereby granted, free of charge, to any person obtaining a copy of this software to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies, subject to the condition that the above copyright notice and this permission notice appear in all copies.
