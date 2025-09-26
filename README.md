# soxutil

> A tiny swiss-army CLI script for Linux that makes common stuff like volume, wifi, bluetooth, music, screenshots, and system info **actually easy**.  

---

##  Why?

I remember sitting there on Arch (btw) thinking:  
- *“wtf is the `bt` command?”*  
- *“how tf do I connect to Wi-Fi without clicking the tray icon?”*  
- *“why do I need to type `wpctl set-volume -l 1 @DEFAULT_AUDIO_SINK@ 0.9` just to change volume??”*  

So I made **`soxutil`** — a single command that wraps all the random system tools into something human.  

---

##  Features

- **Volume**: `soxutil vol 70`, `soxutil vol mute`, `soxutil vol status`  
- **Workspaces** (Hyprland / Sway): `soxutil wrkspc 3`, `soxutil wrkspc list`, `soxutil wrkspc send 2`  
- **Music** (MPRIS): `soxutil msc play`, `soxutil msc seek 60`, `soxutil msc status`  
- **Refresh setup**: `soxutil refresh` (reloads bar, wallpaper, daemons)  
- **Wi-Fi**: `soxutil net list`, `soxutil net connect bsn`, `soxutil net disconnect`  
- **Bluetooth**: `soxutil bt list`, `soxutil bt connect airpods`  
- **System info**: `soxutil sys`  
- **Screenshots**: `soxutil scrot f` (full), `soxutil scrot w` (window), `soxutil scrot s` (selection)  
- **Setup**: `soxutil setup` installs everything, copies script, and even installs the man page  

---

## 📦 Installation

```bash
git clone https://github.com/you/soxutil
cd soxutil
chmod +x soxutil
./soxutil setup
````

That’s it. After this:

* Run `soxutil` from anywhere
* Run `man soxutil` to see the man page

---

##  Examples

```bash
soxutil vol +10         # bump volume up
soxutil net connect jio # fuzzy connect Wi-Fi
soxutil bt connect buds # fuzzy connect bluetooth
soxutil scrot s         # screenshot a region
```

---

##  Dependencies

The `setup` command installs everything you need, but here’s what’s under the hood:

* `playerctl`
* `wpctl` / PipeWire
* `nmcli` (NetworkManager)
* `bluetoothctl` (BlueZ)
* `grim`, `slurp` (Wayland screenshots)
* `jq`, `upower`, `man-db`

---

## ✨ Why use this?

Because typing `soxutil vol mute` is way nicer than memorizing obscure commands.

``` 
Do you want me to also write a **tiny usage cheat sheet** (like a table of commands → what they do) for the README, or keep it as-is?
```
