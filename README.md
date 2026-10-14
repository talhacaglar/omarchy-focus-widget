# Omarchy Focus widget

> **This is a read-only mirror.** The widget is part of **[Omarchy Focus](https://github.com/talhacaglar/omarchy-focus)**, a pomodoro timer, task queue and site blocker with a TUI and CLI. If you like it, please star the main project: **[⭐ talhacaglar/omarchy-focus](https://github.com/talhacaglar/omarchy-focus)**.

Bar widget for [Omarchy Focus](https://github.com/talhacaglar/omarchy-focus): a live pomodoro countdown in the bar, with a panel for tasks, break controls, the site guard, a daily goal, and a 12-week heatmap. It follows your Omarchy theme and updates through inotify, without polling.

![demo](screenshots/demo.gif)

## Install

The widget is a front end for the `omarchy-focus` CLI, so install that first:

```bash
yay -S omarchy-focus
```

Then add the widget:

```bash
omarchy plugin add https://github.com/talhacaglar/omarchy-focus-widget.git --enable
```

(`omarchy-focus widget install` does the same from the AUR package and keeps the widget in sync with the CLI version.)

## Remove

```bash
omarchy plugin remove omarchy-focus     # disables the widget and deletes the plugin folder
yay -Rns omarchy-focus                  # optional: remove the CLI too
```

Your tasks and history stay in `~/.local/share/omarchy-focus/` until you delete that folder. The widget never edits your configuration on its own: the bar entry is added only by `omarchy plugin add --enable` or `omarchy plugin enable`.

## Requirements

- Omarchy 4 (Omarchy Shell)
- the [`omarchy-focus`](https://github.com/talhacaglar/omarchy-focus) CLI 0.2.5 or newer (AUR), which also provides the site guard; the guard asks for your password through Omarchy's polkit dialog
- license: MIT

## Use

- click: panel · right-click: start / pause / resume · middle-click: site guard
- keybinding: `omarchy-shell omarchy-focus toggle`
- settings on the widget entry in `~/.config/omarchy/shell.json`: `showIdleCount`, `refreshIntervalSec`, `guardMinutes`, `command`

This repo is a mirror of `src/omarchy_focus/shell_widget/` in the main project. Report issues and send changes there.

MIT
