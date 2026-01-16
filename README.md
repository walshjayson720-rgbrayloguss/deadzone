# Deadwave

Deadwave is a browser-based top-down zombie survival shooter built with pure HTML, CSS, and JavaScript.
The game uses a multi-page structure with smooth fade transitions to keep performance high and the codebase clean.

---

## Features

* Top-down wave-based zombie combat
* Multiple enemy types (normal, fast, tank, boss)
* Perk system with stacking upgrades
* Perk shop between waves
* Player health regeneration
* Zombie health bars
* Mouse-following animated crosshair
* Fire-rate-based shooting
* Smooth page fade transitions
* Background music with volume control
* Fully compatible with GitHub Pages

---

## Project Structure

```
/deadwave
│
├── index.html        Main menu
├── game.html         Gameplay (canvas + HUD)
├── shop.html         Perk selection screen
├── settings.html    Settings page
│
├── css/
│   └── style.css     All shared styles + fade effects
│
├── js/
│   ├── main.js       Page navigation + transitions
│   ├── game.js       Core game logic and loop
│   ├── perks.js      Perk logic and stacking
│   └── audio.js      Background music
│
└── README.md
```

---

## Page Transitions

Deadwave uses CSS-based fade transitions to make page navigation feel seamless.

### How it works

* Pages fade in on load
* Pages fade out before navigation
* No game logic is affected

### Transition code (simplified)

```css
body {
  opacity: 0;
  transition: opacity 0.4s ease;
}

body.loaded {
  opacity: 1;
}
```

```js
function fadeTo(page){
  document.body.classList.remove("loaded");
  setTimeout(() => {
    location.href = page;
  }, 400);
}
```

---

## Controls

* **WASD** — Move
* **Mouse** — Aim
* **Left Click** — Shoot

---

## Perks

* **+1 Damage** — Bullets deal more damage
* **Faster Regen** — Health regenerates faster
* **Faster Fire Rate** — Reduces shoot cooldown
* **+Speed** — Increases movement speed

Perks stack permanently until death.

---

## Game Flow

1. Start on the main menu
2. Play waves of zombies
3. After each wave, choose a perk
4. Survive as long as possible
5. On death, return to main menu

---

## Running the Game

### Local

Just open `index.html` in a browser.

### GitHub Pages

1. Push the project to a GitHub repository
2. Go to **Settings → Pages**
3. Set source to the `main` branch
4. Open the generated GitHub Pages link

---

## Tech Stack

* HTML5 Canvas
* Vanilla JavaScript
* CSS3
* No frameworks
* No build tools

---

## Future Ideas

* Weapons system
* Save progress with localStorage
* Sound effects
* Difficulty modes
* Mobile controls
* Leaderboards

---

## License

Free to use, modify, and learn from.

---

Deadwave was built as a learning-focused browser game with performance and simplicity in mind.
