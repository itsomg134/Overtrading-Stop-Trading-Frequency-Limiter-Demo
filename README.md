# Overtrading Stop – Trading Frequency Limiter Demo

[![Demo](https://img.shields.io/badge/Demo-Live-brightgreen?style=for-the-badge)](https://html-preview.github.io/?url=https://github.com/yourusername/overtrading-stop/blob/main/index.html)
[![Made with](https://img.shields.io/badge/Made%20with-HTML%20%7C%20CSS%20%7C%20JS-blue?style=for-the-badge)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

<p align="center">
  <img src="https://img.shields.io/badge/Status-Prototype-orange" alt="Status">
  <img src="https://img.shields.io/badge/Platform-Web-lightgrey" alt="Platform">
  <img src="https://img.shields.io/badge/Focus-Risk%20Management-important" alt="Focus">
</p>


## Overview

**Overtrading Stop** is a lightweight, browser-based demo application that simulates a **trade frequency limiter** – a essential risk management tool for traders. It visually demonstrates how an automated stop mechanism can prevent overtrading and revenge trading by enforcing a strict daily trade limit.

>  **Educational Demo Only** – This is not a trading platform or financial advisor. It's a visual prototype for risk management concepts.

![Demo Screenshot](https://via.placeholder.com/700x400?text=Overtrading+Stop+Demo+Interface)

---

##  Features

- ** Daily Trade Limit** – Preconfigured with a 5-trade maximum per day
- ** Real-time Progress Tracking** – Visual progress bar and remaining trades counter
- ** Automatic Stop Engagement** – Instantly blocks new trades when limit is reached
- ** One-Click Reset** – Simulate a new trading day
- ** Simulated Trade Actions** – "Execute Trade" and "Win" buttons for realistic interaction
- ** Professional UI** – Dark mode, cyberpunk-inspired trading dashboard aesthetic
- ** Fully Responsive** – Works on desktop, tablet, and mobile

## Live Demo

**[ Try the Live Demo](https://html-preview.github.io/?url=https://github.com/yourusername/overtrading-stop/blob/main/index.html)**

*Click the link above to see the app in action instantly – no installation required!*



## Installation & Usage

### Option 1: One-Click Web Run
1. Download the `index.html` file
2. Double-click to open in any modern web browser
3. Start simulating trades!

### Option 2: Clone Repository
```bash
git clone https://github.com/yourusername/overtrading-stop.git
cd overtrading-stop
open index.html  # or double-click the file
```

### Option 3: Embed in Your Project
```html
<!-- Copy the entire HTML file content or embed as component -->
<iframe src="path/to/overtrading-stop.html" width="700" height="650"></iframe>
```

---

## How It Works

```javascript
// Core logic (simplified)
const MAX_TRADES = 5;
let currentTrades = 0;
let stopEngaged = false;

function executeTrade() {
  if (currentTrades < MAX_TRADES) {
    currentTrades++;
    updateUI();
  }
  
  if (currentTrades >= MAX_TRADES) {
    stopEngaged = true;  //  Overtrading stop activated
    disableTradingButtons();
  }
}
```

**User Flow:**
1. Start with 0/5 trades executed
2. Click **Execute Trade** or **Win** → counter increases
3. Progress bar fills and remaining trades decrease
4. At 5 trades → **Overtrading Stop** engages instantly
5. All trade buttons disabled with red alert banners
6. Click **Reset Day** to clear counter and release stop

---

##  Interface Components

| Component | Description |
|----------|-------------|
| **Daily Limit Card** | Shows maximum allowed trades (configurable) |
| **Remaining Trades** | Real-time count of available trades |
| **Usage Progress Bar** | Visual fill percentage toward limit |
| **Trade Counter** | Large display of today's executed trades |
| **Stop Indicator** | Pulsing red alert when overtrading is blocked |
| **Action Buttons** | Trade, Win (counts as trade), Reset Day |


## Customization

Easily modify the daily trade limit:

```javascript
// Line ~190 in index.html
const MAX_TRADES = 5;  // Change this to any number
```

**Other tweakable parameters:**
-  Color scheme – Edit CSS variables in `style` block
-  Cooldown behavior – Modify conditional logic in `addTrade()`
-  Additional metrics – Extend the `stat-block` components

---

## Why Overtrading Protection?

> "The market will always be there tomorrow. Capital might not."

**Overtrading** is one of the most common reasons retail traders blow up accounts. Common causes:
-  Revenge trading after losses
-  Gambling mentality vs. edge-based trading  
-  24/7 mobile access with zero friction
-  Lack of personal risk limits

This demo visualizes how **automated hard stops** can enforce discipline and preserve capital.

---

##  Project Structure

```
overtrading-stop/
│
├── index.html           # Complete standalone application
├── README.md           # You are here
├── LICENSE            # MIT License
└── assets/           # Optional (screenshots, demo gif)
    └── demo-preview.png
```

*Zero dependencies – pure HTML5, CSS3, vanilla JavaScript*

---

##  Browser Support

| Browser | Support |
|---------|---------|
| Chrome  |   Full |
| Firefox |   Full |
| Safari  |   Full |
| Edge    |   Full |
| Opera   |   Full |
| Mobile  |  Responsive |

---

##  Contributing

Contributions are welcome! Feel free to:

-  Report bugs
-  Suggest features (e.g., time-based cooldown, custom limits UI)
-  Improve design
-  Enhance documentation

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

##  License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

## 🙏 Acknowledgments

- Inspired by risk management systems in professional trading platforms
- UI design influenced by modern trading dashboards
- Built with vanilla JS – no frameworks, no bloat

---

## 📬 Contact

**Your Name** – [@yourtwitter](https://twitter.com/yourtwitter) – email@example.com

Project Link: [https://github.com/yourusername/overtrading-stop](https://github.com/yourusername/overtrading-stop)

---

<p align="center">
  <strong>Trade smart. Stay disciplined. Know your limits.</strong><br>
  <sub> This app won't stop you from overtrading IRL – but hopefully it inspires better habits.</sub>
</p>

---

## 🔮 Future Roadmap

- [ ] **Time-based cooldown** – Block trades for X minutes after hitting limit
- [ ] **Weekly/Monthly limits** – Multiple timeframe tracking
- [ ] **Trade journal export** – CSV download of session
- [ ] **Customizable limit slider** – User-defined daily max
- [ ] **Multiple themes** – Light mode, colorblind friendly
- [ ] **Win/Loss tracking** – Separate from trade count
- [ ] **Sound alerts** – Optional audio warnings
