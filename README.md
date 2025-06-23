# 🎨 ThemeSwitcher.js

**The simplest way to add light/dark mode to any website — elegant, accessible, and dependency-free.**  

---

## 🌗 Overview

`ThemeSwitcher.js` is a minimalist JavaScript library to help you quickly implement dark and light theme switching in your web app. It automatically detects system preferences, stores user selections in `localStorage`, and allows full customization through CSS variables.

Lightweight, framework-agnostic, and ready to plug into any project.

---

## ✨ Features

- 🌙 **Dark mode / Light mode** switching with one line
- ⚙️ **Auto-detects** system preferences (`prefers-color-scheme`)
- 💾 **Remembers user selection** with `localStorage`
- 🎛️ **Custom themes** using CSS variables
- 🧠 **Clean API**: `ThemeSwitcher.toggle()`, `setTheme()`, `getTheme()`
- 🎯 **Accessible & responsive** – Works with keyboard or toggle button
- 📦 **< 5KB minified**, zero dependencies

---

## 🔧 Installation

### CDN

```html
<script src="https://unpkg.com/themeswitcher.js"></script>
<link rel="stylesheet" href="https://unpkg.com/themeswitcher.js/themeswitcher.css" />
````

### NPM

```bash
npm install themeswitcher.js
```

Then:

```js
import ThemeSwitcher from 'themeswitcher.js';
import 'themeswitcher.js/themeswitcher.css';
```

---

## 🚀 Quick Start

```html
<button id="toggleTheme">Switch Theme</button>

<script>
  ThemeSwitcher.init({
    autoDetect: true,
    defaultTheme: 'light',
    onThemeChange: (theme) => {
      console.log('Current theme:', theme);
    }
  });

  ThemeSwitcher.bindToggle('#toggleTheme');
</script>
```

---

## 📘 API Reference

### `ThemeSwitcher.init(options?)`

Initializes the theme switcher.

| Option          | Type       | Default   | Description                                 |
| --------------- | ---------- | --------- | ------------------------------------------- |
| `autoDetect`    | `boolean`  | `true`    | Detects system theme if no preference saved |
| `defaultTheme`  | `string`   | `'light'` | Default fallback theme                      |
| `onThemeChange` | `function` | `null`    | Callback when theme changes                 |

---

### `ThemeSwitcher.toggle()`

Toggles between `'light'` and `'dark'`.

---

### `ThemeSwitcher.setTheme(theme)`

Sets theme manually.

```js
ThemeSwitcher.setTheme('dark');
```

---

### `ThemeSwitcher.getTheme()`

Returns the currently active theme (`'light'` or `'dark'`).

---

### `ThemeSwitcher.bindToggle(selector)`

Binds a click event to a toggle button.

```js
ThemeSwitcher.bindToggle('#myToggleBtn');
```

---

## 🎨 Customizing Themes

Use CSS variables to define your light/dark theme styles:

```css
:root {
  --bg-color: #ffffff;
  --text-color: #000000;
}

[data-theme="dark"] {
  --bg-color: #1a1a1a;
  --text-color: #f0f0f0;
}
```

Apply them in your app:

```css
body {
  background-color: var(--bg-color);
  color: var(--text-color);
}
```

---

## 📂 Project Structure

```
themeswitcher.js/
├── themeswitcher.js        # Main library
├── themeswitcher.css       # Default themes via CSS variables
├── examples/
│   └── index.html          # Working demo
├── README.md
└── package.json
```

---

## 💡 Use Cases

* Developer portfolios 🧑‍💻
* Documentation sites 📚
* Admin dashboards 📊
* Blogs and publications ✍️

---

## 📜 License

MIT — Use it freely and star it if you like it!
Built with ❤️ by [@holasoymalva](https://github.com/holasoymalva)

---

## ⭐ Like it? Star it!

If you find this helpful, give it a ⭐ on GitHub or share it with fellow devs!
