# Niri dotfiles

Personal Niri desktop config and related files.

## Contents

- `.config/niri/config.kdl` - Niri config
- `.config/waybar/` - Waybar config/style
- `.config/fuzzel/fuzzel.ini` - Fuzzel config
- `.config/wlogout/` - wlogout layout/style
- `.local/bin/` - helper scripts used by Niri/Waybar

## Dependencies

Packages/tools used by this setup (Arch names where applicable):

- `niri`
- `waybar`
- `fuzzel`
- `swaybg`
- `swaylock`
- `wlogout`
- `dunst`
- `wob`
- `udiskie`
- `copyq`
- `ghostty`
- `brightnessctl`
- `playerctl`
- `wireplumber` / `wpctl`
- `networkmanager` / `nmcli`
- `python` (for `wallpaper-cycle`)
- `pywal` / `wal` (used by `wallpaper-cycle`)

## Install

Copy files into your home directory, preserving paths, then make scripts executable:

```bash
cp -r .config .local ~/
chmod +x ~/.local/bin/{wob-daemon,waybar-wrapper,fuzzel,wallpaper-cycle,waybar-workspaces,wifi-menu,bandwidth,volume-overlay}
```

Review paths before using: several files contain `/home/naruto/...` hardcoded paths.

## Notes

- `wallpaper-cycle` rewrites Waybar/Fuzzel/wlogout styles and `waybar-workspaces` when changing wallpapers; expect git diffs after theme changes.
- Runtime artifacts like `~/.cache/current-wallpaper` and wal cache are intentionally not tracked.
