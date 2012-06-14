solarized-termcolor-osc4
========================

Set your terminal&#39;s ANSI color palette to that of the Solarized color
scheme using terminal escape sequences.

This uses OSC 4 to assign color values.  It should work with many terminal
emulators, but not all of them.

Known to work:
- Chrome/ChromeOS Secure Shell

Applications like vim have a tendency to reset all the terminal colors to
their defaults when they run.  I don't have a full solution to this yet, but
for the specific case of vim, you can get a decent solution by putting this
in your .vimrc:

```viml
let g:solarized_termcolors=256
let g:solarized_termtrans=1
colorscheme solarized
```

This tells vim to use the closest equivalent colors to the Solarized palette
in the 256color palette, and not to touch the terminal's background color at
all.

For the time being, you are on your own for fixes to other apps that mess
with the color palette.  Please contribute fixes here if you find them!