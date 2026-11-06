# Omarchy Cheatsheet for Windows Users

**Super** = the Windows-logo key. In Omarchy almost every system shortcut starts with Super.

> **Can't remember a key?** Press **Super + K** to search every keybinding on your machine. This is the most useful shortcut to learn first.
>
> ⚠️ **Watch out:** **Ctrl + Alt + Del** does *not* open a security screen in Omarchy. It **closes all windows**. Use **Super + Escape** for the lock/restart/shutdown menu.

---

## 1. Getting around (start menu, settings, help)

| Action | Windows | Omarchy |
|---|---|---|
| Open the Start menu / search for and launch an app | `Win` or `Win + S` | `Super + Space` |
| Open Settings / control panel | `Win + I` | `Super + Alt + Space` (Omarchy menu) |
| Show all keyboard shortcuts | — | `Super + K` |
| Power menu (lock, suspend, restart, shut down) | `Ctrl + Alt + Del` | `Super + Escape` |
| Lock the screen | `Win + L` | `Super + Ctrl + L` |
| Emoji picker | `Win + .` | `Super + Ctrl + E` |
| Task Manager | `Ctrl + Shift + Esc` | `Super + Space`, then type `btop` |

---

## 2. Launching apps

| Action | Windows | Omarchy |
|---|---|---|
| Terminal | `Win + X` → Terminal | `Super + Return` |
| Text editor (Neovim) | Start → Notepad | `Super + Shift + N` |
| Web browser | Taskbar / Start | `Super + Shift + Return` |
| File manager | `Win + E` | `Super + Shift + F` |
| Run any program by name | `Win + R` | `Super + Space` |

---

## 3. Window management

Omarchy uses **tiling**: new windows sit side by side and fill the screen, so you seldom drag or resize windows by hand.

| Action | Windows | Omarchy |
|---|---|---|
| Close the window | `Alt + F4` | `Super + W` |
| Maximize / fullscreen | `Win + ↑` | `Super + F` |
| Full width (bar stays visible) | — | `Super + Alt + F` |
| Make a window float (normal overlapping window) | — (default) | `Super + T` (toggle tiled ↔ floating) |
| Pin a floating window on top of everything | — | `Super + O` |
| Switch focus to another window | `Alt + Tab` | `Super + ←/→/↑/↓` |
| Snap/move the window left, right, up, down | `Win + ←/→` | `Super + Shift + ←/→/↑/↓` (swaps with the neighbour) |
| Make the window wider / narrower | Drag the edge | `Super + =` / `Super + -` |
| Make the window taller / shorter | Drag the edge | `Super + Shift + =` / `Super + Shift + -` |
| Group windows as tabs | — | `Super + G` |
| Hide a window in the "scratchpad" | Minimize (`Win + ↓`) | `Super + Alt + S` |
| Bring back the scratchpad | Click the taskbar | `Super + S` |

---

## 4. Workspaces (virtual desktops)

Workspaces are numbered and created on demand. You don't need to "add a desktop"; just jump to a number.

| Action | Windows | Omarchy |
|---|---|---|
| Go to desktop / workspace *N* | `Win + Ctrl + ←/→` | `Super + 1…9` |
| Next workspace | `Win + Ctrl + →` | `Super + Tab` |
| Previous workspace | `Win + Ctrl + ←` | `Super + Shift + Tab` |
| Return to the last workspace you were on | — | `Super + Ctrl + Tab` |
| Create a new desktop | `Win + Ctrl + D` | Just press `Super + <unused number>` |
| Move the window to workspace *N* (and follow it) | `Win + Tab`, then drag | `Super + Shift + 1…9` |
| Move the window to workspace *N* (stay where you are) | — | `Super + Shift + Alt + 1…9` |
| Overview of all windows | `Win + Tab` | — (use `Super + 1…9` to jump) |

---

## 5. Multiple monitors

In Omarchy, each monitor shows its own workspace. You move windows between screens by moving them (or their whole workspace) to that screen.

| Action | Windows | Omarchy |
|---|---|---|
| Move focus to the next monitor | Mouse | `Ctrl + Alt + Tab` |
| Move focus to the previous monitor | Mouse | `Ctrl + Alt + Shift + Tab` |
| Move the window to the other monitor | `Win + Shift + ←/→` | `Super + Shift + <number of a workspace shown on that monitor>` |
| Move the whole workspace (and every window in it) to another monitor | — | `Super + Shift + Alt + ←/→/↑/↓` |
| Monitor layout, resolution, scaling | Settings → Display | `Super + Alt + Space` → Setup → Monitors |

---

## 6. Clipboard & screenshots

Omarchy's **Super** clipboard keys work everywhere, including the terminal (but not the file manager). Plain `Ctrl + C/V` still works in most graphical apps.

| Action | Windows | Omarchy |
|---|---|---|
| Copy | `Ctrl + C` | `Super + C` |
| Cut | `Ctrl + X` | `Super + X` (not in terminal) |
| Paste | `Ctrl + V` | `Super + V` |
| Clipboard history | `Win + V` | `Super + Ctrl + V` |
| Screenshot (select area, then edit) | `Win + Shift + S` | `Print Screen` |
| Screenshot straight to clipboard | `Print Screen` | `Shift + Print Screen` |
| Start / stop screen recording | `Win + Alt + R` | `Alt + Print Screen` |
| Colour picker | PowerToys `Win + Shift + C` | `Super + Print Screen` |

> In the terminal, `Ctrl + C` **stops the running program**; it does not copy. Use `Super + C`.

---

## 7. Editing documents (Notepad → Neovim)

Omarchy's default editor is **Neovim**, preconfigured as **LazyVim**. Open it with `Super + Shift + N`, or from a terminal with `nvim filename.txt`.

### The one idea you must know: modes
- **Normal mode** (the default): keys are *commands*, not text. Press **`Esc`** to return here at any time.
- **Insert mode**: you type normally like Notepad. Press **`i`** to enter it.
- **Command line**: from Normal mode, type **`:`** followed by a command and press `Enter`.

If something strange happens, press `Esc` a couple of times and you're back in Normal mode.

### Basic commands

| Action | Notepad (Windows) | Neovim (Normal mode unless noted) |
|---|---|---|
| Start typing text | Just type | `i` (insert at cursor), `o` (new line below) |
| Stop typing / go back to commands | — | `Esc` |
| Save | `Ctrl + S` | `Ctrl + S` (works in LazyVim) or `:w` |
| Save as | `Ctrl + Shift + S` | `:w newname.txt` |
| Quit | `Alt + F4` | `:q` |
| Save and quit | — | `:wq` |
| Quit **without** saving | "Don't save" | `:q!` |
| Open a file | `Ctrl + O` | `Space Space` (fuzzy file finder) or `:e filename` |
| Show the file-tree sidebar | — | `Space e` |
| Undo | `Ctrl + Z` | `u` |
| Redo | `Ctrl + Y` | `Ctrl + R` |
| Find | `Ctrl + F` | `/text` then `Enter`; `n` = next, `N` = previous |
| Find and replace (whole file) | `Ctrl + H` | `:%s/old/new/g` |
| Search text in all project files | `Ctrl + Shift + F` (VS Code) | `Space s g` |
| Select text | `Shift + arrows` | `v` then move with arrows (`V` = whole lines) |
| Select all | `Ctrl + A` | `ggVG` |
| Copy selection | `Ctrl + C` | `y` |
| Cut / delete selection | `Ctrl + X` | `d` |
| Paste | `Ctrl + V` | `p` |
| Copy the whole line | — | `yy` |
| Cut the whole line | `Home`, `Shift + End`, `Ctrl + X` | `dd` |
| Go to the top / bottom of file | `Ctrl + Home` / `Ctrl + End` | `gg` / `G` |
| Go to line 42 | `Ctrl + G` | `:42` |
| Next / previous open file (tab) | `Ctrl + Tab` | `Shift + L` / `Shift + H` |
| Close the current file (tab) | `Ctrl + W` | `Space b d` |
| Jump between sidebar and editor | — | `Ctrl + W` then `w` |
| Git status / commit view | — | `Space g g` |

LazyVim shares the system clipboard, so text copied with `y` can be pasted into other apps, and the mouse works for clicking and selecting.

**Tip:** Run `:Tutor` inside Neovim for a 30-minute interactive lesson. The full LazyVim key list is at <https://www.lazyvim.org/keymaps>.

**Prefer a Notepad-style editor?** Install a different one from `Super + Alt + Space` → Install → Editor, then make it the default under Setup → Defaults.

---

## 8. Terminal commands (Command Prompt / PowerShell → Linux)

| Task | Windows | Omarchy (Linux) |
|---|---|---|
| List files | `dir` / `ls` | `ls` (`ls -la` shows hidden files and details) |
| Change folder | `cd` | `cd` (`cd ~` = home folder, `cd ..` = up one) |
| Show the current folder | `cd` / `pwd` | `pwd` |
| Copy a file | `copy` | `cp source dest` (`cp -r` for folders) |
| Move / rename | `move` / `ren` | `mv old new` |
| Delete a file | `del` | `rm file` (`rm -r` for folders; there is no Recycle Bin) |
| Make a folder | `mkdir` | `mkdir name` |
| Show file contents | `type` | `cat file` |
| Clear the screen | `cls` | `clear` or `Ctrl + L` |
| Network info | `ipconfig` | `ip a` |
| Run as administrator | "Run as admin" | Prefix the command with `sudo` |
| Install software | Microsoft Store / winget | `Super + Alt + Space` → Install, or `yay -S package` |
| Update the system | Windows Update | `Super + Alt + Space` → Update, or `omarchy-update` |
| Stop a running command | `Ctrl + C` | `Ctrl + C` |
| Paste into the terminal | `Ctrl + V` | `Super + V` (or `Ctrl + Shift + V`) |

---

*Defaults as of Omarchy's hotkeys manual (November 2026). Your own overrides or a future update can change them; `Super + K` always shows what's on your machine.*
