# gnome-dconf

## vim-keybindings

Adds the possibility to use Vim-style `[hjkl]` instead of arrows in Gnome
keyboard shortcuts.

| Action                               | Keybinding                 |
|--------------------------------------|----------------------------|
| Cycle window in application switcher | `<Alt>[hl]`				|
| Switch between workspaces            | `<Ctrl><Alt>[hjkl]`        |
| Move window to a different workspace | `<Ctrl><Alt><Shift>[hjkl]` |
| Move window to a different monitor   | `<Super><Shift>[hjkl]`     |
| Maximize/unmaximize window           | `<Super>[jk]`              |
| Tile window left/right               | `<Super>[hl]`              |

To add the keybindings to your settings run:
```
dconf load / < vim-keybindings
```

The default shortcuts will be left intact so arrows can still be used instead of
`[hjkl]`.  An exception is `<Super>l` and `<Super>h` which is normally used for
locking the screen and minimizing windows.  These are now used for tiling left
and right.

While we're at it, I also recommend adding the following to your `.vimrc` such
that `<Ctrl>[hjkl]` can be used to change window _within_ Vim.

```
nnoremap <C-h> <C-W><C-h>
nnoremap <C-j> <C-W><C-j>
nnoremap <C-k> <C-W><C-k>
nnoremap <C-l> <C-W><C-l>
```

## custom-keybindings

A few custom keybindings I use a lot:

| Action              | Keybinding                  |
|---------------------|-----------------------------|
| Open web browser    | `<Super>w`                  |
| Open e-mail client  | `<Super>e`                  |
| Open file browser   | `<Super>f`                  |
| Open terminal       | `<Super>t`                  |
| Spawn terminal      | `<Super>y`                  |

By spawning a terminal I mean that you keep the current working directory of an already active terminal window.


To add the keybindings to your settings run:
```
dconf load / < custom-keybindings
```

## Disclaimer

This is provided as-is with no guarantee whatsoever. I may not be held liable for any undesirable outcome of its use. However, if you do find issues, I'd be glad if you put up an issue.
