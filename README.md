# Z-CITY ROLEPLAY — Gmod Loading Screen

A GTA V–style loading screen for your Garry's Mod server, built for GitHub Pages.

## 📁 File Structure

```
z-city-loading/
├── index.html          ← Main loading screen
└── assets/
    ├── bg1.jpg         ← Background image 1
    ├── bg2.jpg         ← Background image 2
    ├── bg3.jpg         ← Background image 3
    └── theme.ogg       ← Background music
```

## 🚀 GitHub Pages Setup

1. Create a new GitHub repository (e.g. `z-city-loading`)
2. Upload all files — keep the `assets/` folder structure intact
3. Go to **Settings → Pages**
4. Set source to `Deploy from branch` → `main` → `/ (root)`
5. Save — your page will be live at:
   `https://YOUR_USERNAME.github.io/z-city-loading/`

## 🎮 Gmod Integration

In your Gmod server's `server.cfg` or Lua config, set the loading URL:

```lua
-- In your gamemode or addons:
-- garrysmod/cfg/server.cfg
sv_loadingurl "https://YOUR_USERNAME.github.io/z-city-loading/"
```

Or via Lua:
```lua
-- In lua/autorun/server/loadingurl.lua
hook.Add("Initialize", "SetLoadingURL", function()
    RunConsoleCommand("sv_loadingurl", "https://YOUR_USERNAME.github.io/z-city-loading/")
end)
```

## ✏️ Customization

- **Server name / description** — edit the `#info-block` section in `index.html`
- **Slideshow speed** — change `6000` (ms) in the `setInterval` call
- **Background images** — replace `bg1.jpg`, `bg2.jpg`, `bg3.jpg` in `/assets/`
- **Music** — replace `theme.ogg` in `/assets/`
- **Progress bar** — the bar is cosmetic/fake for loading screens; Gmod handles actual loading
