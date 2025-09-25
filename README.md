# $STUDY Stock Tracker

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with: HTML, CSS, JS](https://img.shields.io/badge/Made%20with-HTML%2C%20CSS%2C%20JS-blue.svg)](https://developer.mozilla.org/)
[![Chart Library: ApexCharts.js](https://img.shields.io/badge/Charts-ApexCharts.js-green.svg)](https://apexcharts.com/)

A single-file, zero-dependency web app that turns your study sessions into a personal stock market. Gamify your learning, stay motivated, and visualize your progress with live-updating candlestick and line charts.



## 🚀 About This Project

Studying can sometimes feel like a grind. This project was built to make it more interesting and engaging by applying the principles of a stock market to your learning process.

Every correct answer, completed chapter, or moment of deep understanding pushes your personal `$STUDY` stock price up. Conversely, mistakes and distractions will cause the price to dip. With a bit of built-in randomness to simulate "market volatility," you get a dynamic and visually rewarding way to track your effort and knowledge growth.

Best of all? It's all contained in a **single HTML file**. No installations, no servers, no setup required. Just download and open.

## ✨ Features

- **Single HTML File:** The entire application is self-contained. Easy to download, use, and share.
- **Interactive Charting:** Visualize your study history with beautiful candlestick or line charts, powered by ApexCharts.js.
- **Button-Driven Interface:** No manual data entry. Just click buttons for different study actions (`Correct Answer`, `Distracted`, etc.).
- **Market Volatility:** At the start of each session, a random "market sentiment" is generated, applying multipliers to gains or losses to keep things exciting.
- **Persistent Local Storage:** Your study history is automatically saved in your browser's `localStorage`. Close the tab and your progress will be there when you return.
- **Session Tracking:** Each study period is treated like a "trading day" with Open, High, Low, and Close prices.
- **Data Reset:** A built-in function to safely reset all your data and start fresh.

## 🛠️ How to Use

1.  **Download:** Download the `study-tracker.html` file from this repository.
2.  **Open:** Open the file in any modern web browser (like Chrome, Firefox, or Edge).
3.  **Study!**
    - Click **`🚀 Start New Session`** to begin.
    - As you study, click the corresponding buttons to reflect your actions.
    - Watch your `$STUDY` price update in real-time.
    - Click **`🛑 End Session`** when you're done. A new candle will be added to your chart.

## 📈 The Rules of the $STUDY Stock Market

The price of your `$STUDY` stock is determined by your actions. Here are the default rules:

### Positive Events (Price UP)

| Action | Base Price Change |
| :--- | :--- |
| **✓ Correct Sub-Part** | `+$0.50` |
| **✓✓ Correct Full Question** | `+$2.00` |
| **★ Mastered Concept** | `+$5.00` |
| **🏆 Complete Paper/Chapter**| `+$10.00` |

### Negative Events (Price DOWN)

| Action | Base Price Change |
| :--- | :--- |
| **✗ Wrong Sub-Part** | `-$0.75` |
| **✗✗ Wrong Full Question** | `-$3.00` |
| **! Conceptual Gap** | `-$8.00` |
| **📱 Distracted** | `-$5.00` |

### 🎲 Market Volatility

At the start of each session, a random event is triggered that affects the multipliers for that session only.

| Roll (1-6) | Sentiment | Effect |
| :--- | :--- | :--- |
| 1 | **Market Crash** | All losses are **doubled**. |
| 2 | **Bear Market** | All losses are multiplied by **1.5x**. |
| 3 | **Stable Market** | No change. |
| 4 | **Bull Market** | All gains are multiplied by **1.5x**. |
| 5 | **Market Rally** | All gains are **doubled**. |
| 6 | **Supernova** | All gains are **tripled!** |

## 🔧 How It Works & Customization

The entire application is built with vanilla **HTML**, **CSS**, and **JavaScript**.

- **Structure:** The HTML provides the basic layout of the dashboard.
- **Styling:** All styles are contained within the `<style>` tag in the `<head>` of the document. You can easily change colors by editing the `:root` variables.
- **Logic:** The core application logic resides in the `<script>` tag at the end of the `<body>`.
- **Charting:** The [ApexCharts.js](https://apexcharts.com/) library is loaded from a CDN for creating the charts.
- **Data Storage:** Your data is stored as a JSON string in your browser's `localStorage` under the key `studyHistory`.

To customize the rules, simply open the `.html` file in a text editor and find the `handleAction` function calls within the JavaScript section. You can change the base values to whatever you like!

```javascript
// Example: Find this line in the script
document.getElementById('correctFull').addEventListener('click', () => handleAction(2.00));

// Change 2.00 to 3.00 to make full questions worth more
document.getElementById('correctFull').addEventListener('click', () => handleAction(3.00));
```

## ❤️ Acknowledgments

- This project relies on the fantastic and easy-to-use [ApexCharts.js](https://apexcharts.com/) library for all charting functions.

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

```
