# XQUICKLAUNCH
- A simple command launcher using shortcut keys.

## Synopsis
- `xquicklaunch`

## Overview
- This program allows you to execute commands with predefined key bindings.
- Execute this program by adding into the `.xinitrc` or execute `xquicklaunch &` on your terminal emulator.

## Depends
- X11
- python-xlib

## Configures
- The default config file path is `$HOME/.config/xquicklaunch.conf`
- [xquicklaunch.conf](./xquicklaunch.conf)

```
KEY_BINDS = {
    ('1', X.Mod1Mask | X.ControlMask) : 'gnome-terminal &',
    ('2', X.Mod1Mask | X.ControlMask) : 'code &',
    ('3', X.Mod1Mask | X.ControlMask) : 'google-chrome &',
}
```

- Keybindings and commands are defined as Python dictionary items.
  - Each item is described as `(<key>, <modifier_mask>) : <command>`.
  - Add `&` at the end of the command asynchronously.
