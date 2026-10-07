# 🕰️ Analog Clock

A working analog clock built with plain **HTML**, **CSS** and **JavaScript**. The hour, minute and second hands move in real time based on your device's clock.

![HTML5](https://img.shields.io/badge/HTML5-E34C26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

<p align="center"><img src="docs/images/clock.png" alt="Analog clock with hour, minute and second hands" width="300"></p>

## ✨ Features

- Hour, minute and second hands that update every second
- Smooth positioning — the minute hand accounts for seconds, and the hour hand for minutes, so hands sit between numbers like a real clock
- Numbers 1–12 positioned around the clock face with CSS
- No libraries or frameworks

## ⚙️ How It Works

Every second, `script.js` reads the current time and works out how far around the clock each hand should be as a ratio (0–1). It then sets a CSS custom property, `--rotation`, on each hand, and the stylesheet turns that into a `rotate()` transform.

```js
const secondsRatio = currentDate.getSeconds() / 60
const minutesRatio = (secondsRatio + currentDate.getMinutes()) / 60
const hoursRatio   = (minutesRatio + currentDate.getHours()) / 12
```

## 📁 Project Structure

```
├── index.html   # Clock face, hands and numbers
├── styles.css   # Layout, hand styling and rotation
└── script.js    # Time calculation and hand updates
```

## 🚀 Getting Started

No setup needed — clone the repo and open `index.html` in your browser.

```bash
git clone https://github.com/Scarface96/clock-app.git
```

## 📚 What I Learned

DOM selection with data attributes, `setInterval`, the JavaScript `Date` object, and driving CSS transforms from JavaScript using CSS custom properties.

---

👤 **Tony Mulunda** — [GitHub @Scarface96](https://github.com/Scarface96)

## About This Project

A real-time analog clock built with vanilla HTML, CSS and JavaScript. It demonstrates DOM manipulation, JavaScript date/time handling, timed updates and the use of CSS transforms and custom properties to create a dynamic interface.
