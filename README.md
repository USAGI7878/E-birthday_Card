# 🎂 THE BLOW CHALLENGE (吹蜡烛大挑战)

A fun, interactive Web Audio API-powered H5 game! Use your phone or computer's microphone to detect real **blowing power** and blow out the candles on the birthday cake. Be careful—blowing too hard will make the cake shake violently, and blowing too slowly will cause you to run out of oxygen!

这是一个基于 Web Audio API 开发的趣味互动 H5 小游戏！利用手机或电脑的麦克风检测真实的**呼吸/吹气力量**来吹灭生日蛋糕上的蜡烛。小心，用力过猛蜡烛会剧烈摇晃，动作太慢可就会因“缺氧”而挑战失败哦！

---

## ✨ Features / 游戏特色

### 🌍 English Version
* **🎙️ Real Breath Detection**: Connects to the browser's `navigator.mediaDevices.getUserMedia` audio stream and utilizes `AudioContext` to analyze blow volume and frequency in real time.
* **💨 Dynamic Feedback System**:
  * **POWERFUL!**: Perfect blowing intensity, candles will start to go out one by one.
  * **CHILL OUT!**: Blowing too hard triggers an **Extreme Shake** screen animation.
  * **BLOW HARDER!**: Not enough power to put out the fire.
* **🔋 Oxygen Control (O2 Bar)**: The oxygen bar drains while you blow. Fail to put out all 5 candles before it hits 0%, and you'll trigger the **FAINTED! 😵** ending!
* **🎵 Audiovisual Feast**: Packed with background music, a custom celebratory confetti explosion (via Canvas Confetti), and randomized heartfelt/witty birthday blessings.

### 🇨🇳 中文版
* **🎙️ 真实吹气检测**：调用浏览器 `navigator.mediaDevices.getUserMedia` 获取音频流，通过 `AudioContext` 实时分析吹气音量与频率。
* **💨 动态反馈系统**：
  * **POWERFUL!**：完美力度，蜡烛开始一根根被吹灭。
  * **CHILL OUT!**：用力过猛，蛋糕和提示语会产生夸张的**震动特效 (Extreme Shake)**。
  * **BLOW HARDER!**：力度不够，无法吹灭蜡烛。
* **🔋 氧气机制 (O2 Bar)**：游戏开始后，只要检测到吹气就会持续消耗氧气条。如果没能在氧气耗尽前吹灭 5 根蜡烛，就会触发 **FAINTED! 😵 (晕厥)** 结局！
* **🎵 视听盛宴**：内置背景音乐、吹灭烟花纸屑特效（Canvas Confetti）以及随机生成的温馨/幽默生日祝福语。

---

## 🎮 How to Play / 玩法介绍

| 🌍 English | 🇨🇳 中文 |
| :--- | :--- |
| **1. Unlock Mic**: Tap the 🎤 button at the bottom and grant microphone access in the browser popup. | **1. 解锁麦克风**：点击屏幕下方的 🎤 按钮，并在浏览器弹窗中允许网站使用麦克风权限。 |
| **2. Steady Breath**: Blow steadily and firmly into your microphone. | **2. 控制呼吸**：对准麦克风**均匀、用力**地吹气。 |
| **3. Watch out**: Don't scream (it triggers the shake status). Don't be too slow, or the `OXYGEN LEVEL` will run out. | **3. 注意避坑**：不要大喊大叫（会触发暴走摇晃状态）；动作不要太慢，否则顶部的 `OXYGEN LEVEL` 耗尽就会游戏结束。 |
| **4. Win**: Extinguish all 5 candles to unlock the confetti and a random birthday wish! | **4. 收获祝福**：成功吹灭所有蜡烛后，触发彩蛋和祝福。 |

---

## 🛠️ Tech Stack / 技术栈

* **Core Frontend (前端核心)**: HTML5, CSS3 (Flexbox, CSS Animation), Native JavaScript
* **Audio Processing (音频处理)**: Web Audio API (`AudioContext`, `AnalyserNode`)
* **Graphics (图形渲染)**: SVG (Used for rendering the cake and dynamic flames / 用于绘制蛋糕与动态火焰)
* **Effects Library (特效库)**: [canvas-confetti](https://github.com/catdad/canvas-confetti) (For the celebration splash / 五彩纸屑特效)
* **Typography (字体)**: Google Fonts (Spicy Rice)

---

## 🚀 Quick Start / 快速开始

This project is a **single-file pure frontend application**. No installation, no node_modules, just plug and play!
本项目为**单文件纯前端应用**，无需安装任何依赖，即开即玩：

1. Clone or download this repository to your local machine.
   克隆或下载本项目到本地。
2. Double-click `index.html` to run it in your browser. (Mobile browsers or desktop Chrome/Safari are highly recommended for the best microphone experience).
   双击 `index.html` 即可在浏览器中运行（建议在手机端或使用 Chrome/Safari 浏览器以获得最佳麦克风体验）。

> ⚠️ **Note / 注意**: Due to modern browser Autoplay Policies, audio contexts and microphone streams must be initialized through user interaction (like clicking the 🎤 button).
> 由于现代浏览器的安全策略（Autoplay Policy），音频和麦克风权限必须在用户产生交互（如点击页面上的 🎤 按钮）后才能正常启用。

---

## 📝 Customization Tip / 代码自定义提示

If you want to gift this game to a specific friend, you can easily customize the text inside the `blessings` array in the script tag:
如果您想将这个小游戏送给特定的朋友，可以修改代码中的 `blessings` 数组：

```javascript
const blessings = [
    "Write your custom message for your friend here...",
    "在这里写下你想对 TA 说的第一句定制祝福...",
    "Stay sharp. This year, take up more space — you’ve earned it."
];
