# 💌 Valentine's Puzzle

An interactive sliding puzzle website to ask your special someone to be your Valentine!

## ✨ Features

- 💌 Animated envelope with pulsing glow and romantic title
- 🧩 3x3 sliding puzzle with your custom image
- ⌨️ Typewriter effect on the greeting message
- 💕 Floating hearts background animation
- 💗 Heart-shaped confetti celebration
- 🎵 Background music (plays on envelope open)
- 📱 Fully responsive (works on mobile and desktop)

## 🛠️ Setup

### 1. Add your image tiles

Cut your image into a 3×3 grid and place the 9 PNGs in the `images/` folder:

```
tile-1.png   tile-2.png   tile-3.png
tile-4.png   tile-5.png   tile-6.png
tile-7.png   tile-8.png   tile-9.png
```

- Tiles are numbered left-to-right, top-to-bottom
- `tile-3.png` will be the empty space (top-right) but appears once the puzzle is completed
- Also save the full image as `images/full-image.png`

> **Tip:** You can use Python with Pillow to split the image programmatically:
> ```bash
> poetry install
> poetry run python split_image.py
> ```

### 2. Change the text strings

Edit `index.html` and update the relevant strings:

- Title above the envelope (e.g. *"Para el amor de mi vida"*)
- Puzzle greeting (e.g. *"Querida Meli..."*)
- Completion message (e.g. *"...cada pieza me lleva a vos."*)
- Final question (e.g. *"¿Querés ser mi Valentine?"*)
- Celebration response

### 3. Change the music (optional)

Replace the file in `sounds/` and update the reference in `index.html`:

```html
<audio id="bgMusic" loop preload="auto">
    <source src="sounds/your-song.mp3" type="audio/mpeg">
</audio>
```

### 4. Deploy to GitHub Pages

1. Push the repository to GitHub
2. Go to **Settings** → **Pages**
3. Source: **Deploy from branch**
4. Branch: `main` (or `master`)
5. Click **Save**

### 5. Share the link!

Your site will be at: `https://YOUR-USERNAME.github.io/your-repo/`

## 🎮 How It Works

| Stage | What happens |
|-------|-------------|
| **0** | Envelope appears with floating hearts and a romantic title |
| **1** | Clicking it opens the envelope, starts the music, and reveals the 3x3 puzzle |
| **2** | Solving the puzzle reveals the full image with your message |
| **3** | Clicking "Yes" → heart confetti and celebration! |

## 🎨 Customization

Everything can be customized by editing `index.html`:

- **Colors:** Look for the CSS values (`#FFDAE9`, `#c41e3a`, etc.)
- **Fonts:** Swap the Google Font by changing the `<link>` in the `<head>`
- **Music volume:** Change `bgMusic.volume = 0.4` (range `0.0` to `1.0`)
- **Celebration GIF:** Replace `dudu.gif` with your own GIF
- **Typewriter speed:** Adjust the `70` in the typewriter `setTimeout`

---

Made with ❤️ for Valentine's Day
