# سر المحيط · Ocean Secret

An interactive companion to the Arabic children's story **«سر المحيط»**: Noah dives under the sea to find the missing golden coral, meeting sea creatures who each teach him a real fact about ocean life.

Kids reach it by scanning the QR code printed on the hard copy of the story.

**▶ Play it here: [shiba3006.github.io/Ocean_game](https://shiba3006.github.io/Ocean_game/)**

The whole experience is in Egyptian Arabic, right-to-left, and made for phones first (ages ~5–10).

---

## What's inside

### 📖 The interactive story
The book is a choose-your-own-adventure, and the web version keeps every page exactly as it was illustrated. Big buttons replace "go to page X":

- At page 4 the reader picks a path: **the octopus cave** 🐙 or **the deep sea** 🦈.
- At page 11 they choose how Noah solves the mystery, which leads to one of **3 endings**.
- Each ending found lights up a shell 🐚 at the top, encouraging kids to read again and find the rest.

### 🎮 The games
Each game is built around one of the story's characters and the real ability they talk about. Winning a game earns a piece of the golden coral. Collect all 4 to restore the coral.

| Game | Character | How it plays | What kids learn |
|---|---|---|---|
| **كشاف نور** | Nour the jellyfish | Move Nour through a dark scene to light it up and find 4 hidden clues | Jellyfish can glow (bioluminescence) |
| **فين تيتو؟** | Teto the octopus | Spot Teto camouflaged on a rock, 5 rounds, each harder | Octopuses change color to hide |
| **رادار سيف** | Seif the shark | Tap the sand; the closer you are, the stronger Seif's signal (hot/cold) | Sharks sense tiny electric signals (ampullae of Lorenzini) |
| **مين بيقول كده؟** | All friends | Read a fact and pick which creature said it | Recap of every creature's talents |

---

## Technical notes

- **One self-contained file.** Everything (story pages, character art, games) lives in `index.html`, with images embedded as WebP data URIs. There's no build step, framework, or server code.
- **Plain HTML, CSS and JavaScript.** The only external request is the Google Font (*Baloo Bhaijaan 2*), with system fallbacks if it doesn't load.
- **Progress is saved on the device** with `localStorage` (endings found and coral pieces won). Nothing is sent anywhere.
- **Hash routing** (`#story`, `#story/7`, `#nour`, …) so the phone's back button works naturally.
- **Direct link to the story:** `https://shiba3006.github.io/Ocean_game/#story`
- Responsive: phones, tablets (portrait and landscape), laptops and large monitors.
- Respects `prefers-reduced-motion`.

### Repository layout

```
index.html           the whole app (story + games)
og-image.png         link-preview image for WhatsApp / Facebook (1200×630)
ocean_game_qr.png    QR code for the printed book
README.md
```

### Running locally

Open `index.html` in any modern browser. No install needed.

### Deploying

The site is served by **GitHub Pages** from the repository root (Settings → Pages → Deploy from branch → `main` / root). Any change pushed to `index.html` goes live within a minute or two.

---

## QR code

`ocean_game_qr.png` points to `https://shiba3006.github.io/Ocean_game/` and carries the «كان يا ما كان» logo in the centre. It's 2700×2700 px with high error correction, so it stays sharp and scannable in print. A printed size of at least **2.5 × 2.5 cm** is recommended, keeping the white border around it.

---

## Credits

A «كان يا ما كان» (Kan Ya Ma Kan) story.


- **Story & illustrations:** Esraa
- **Web story & games:** [Shiba3006](https://github.com/Shiba3006)
