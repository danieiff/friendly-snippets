# Snippets syntax: https://code.visualstudio.com/docs/editor/userdefinedsnippets

- Variables

TM_SELECTED_TEXT The currently selected text or the empty string
TM_CURRENT_LINE The contents of the current line
TM_CURRENT_WORD The contents of the word under cursor or the empty string
TM_LINE_INDEX The zero-index based line number
TM_LINE_NUMBER The one-index based line number
TM_FILENAME The filename of the current document
TM_FILENAME_BASE The filename of the current document without its extensions
TM_DIRECTORY The directory of the current document
TM_FILEPATH The full file path of the current document
RELATIVE_FILEPATH The relative (to the opened workspace or folder) file path of the current document
CLIPBOARD The contents of your clipboard
WORKSPACE_NAME The name of the opened workspace or folder
WORKSPACE_FOLDER The path of the opened workspace or folder
CURSOR_INDEX The zero-index based cursor number
CURSOR_NUMBER The one-index based cursor number

CURRENT_YEAR The current year
CURRENT_YEAR_SHORT The current year's last two digits
CURRENT_MONTH The month as two digits (example '02')
CURRENT_MONTH_NAME The full name of the month (example 'July')
CURRENT_MONTH_NAME_SHORT The short name of the month (example 'Jul')
CURRENT_DATE The day of the month as two digits (example '08')
CURRENT_DAY_NAME The name of day (example 'Monday')
CURRENT_DAY_NAME_SHORT The short name of the day (example 'Mon')
CURRENT_HOUR The current hour in 24-hour clock format
CURRENT_MINUTE The current minute as two digits
CURRENT_SECOND The current second as two digits
CURRENT_SECONDS_UNIX The number of seconds since the Unix epoch
CURRENT_TIMEZONE_OFFSET The current UTC time zone offset as +HH:MM or -HH:MM (example -07:00).

RANDOM 6 random Base-10 digits
RANDOM_HEX 6 random Base-16 digits
UUID A Version 4 UUID

BLOCK*COMMENT_START Example output: in PHP /* or in HTML \<!--
BLOCK*COMMENT_END Example output: in PHP */ or in HTML -->
LINE_COMMENT Example output: in PHP //

# Friendly Snippets

Snippets collection for a set of different programming languages.

The only goal is to have one community driven repository for all kinds of
snippets in all programming languages, this way you can have it all in one
place.

## Install

Use your plugin manager of choice, e.g.

### With Lazy.nvim

```lua
{ "rafamadriz/friendly-snippets" }
```

> **Warning**: If you're using LuaSnip make sure to use
> `require("luasnip.loaders.from_vscode").lazy_load()`, and add
> `friendly-snippets` as a dependency for LuaSnip, otherwise snippets might not
> be detected. If you don't use `lazy_load()` you might notice a slower
> startup-time
>
> ```lua
> {
>   "L3MON4D3/LuaSnip",
>   dependencies = { "rafamadriz/friendly-snippets" },
> }
> ```

### With Packer

```lua
use "rafamadriz/friendly-snippets"
```

### With vim-plug

```vim
Plug "rafamadriz/friendly-snippets"
```

### With coc.nvim

```vim
:CocInstall https://github.com/rafamadriz/friendly-snippets@main
```

## Usage

This collection of snippets should work with any snippet engine that supports
loading vscode snippets. Like for example:

- [vim-vsnip](https://github.com/hrsh7th/vim-vsnip)
- [LuaSnip](https://github.com/L3MON4D3/LuaSnip)
- [coc-snippets](https://github.com/neoclide/coc-snippets)

## Add snippets from a framework to a filetype.

> **Note**: This is handled by your snippet engine and has nothing to do with this snippets collection

There's extra snippets included in this repo but they are not added by default,
since it would be irrelevant for people not using those frameworks. See
[`snippets/frameworks`](https://github.com/rafamadriz/friendly-snippets/tree/main/snippets/frameworks)

For example: if you want to add rails snippets to ruby.

With LuaSnip:

```lua
require'luasnip'.filetype_extend("ruby", {"rails"})
```

With vim-vsnip:

```viml
let g:vsnip_filetypes.ruby = ['rails']
```

## Excluding snippets

> **Note**: This is handled by your snippet engine and has nothing to do with this snippets collection

With LuaSnip, see `help luasnip-loaders`

```lua
-- will exclude all javascript snippets
require("luasnip.loaders.from_vscode").load {
    exclude = { "javascript" },
}
```

## Showcase

### HTML

![HTML gif](https://user-images.githubusercontent.com/67771985/131255337-d53f3408-b60d-44a2-93ba-9a3240a7436e.gif)

### JS

![JS gif](https://user-images.githubusercontent.com/67771985/131255342-e393165a-e4b1-401e-9084-a782b9dd3fef.gif)

## TODO

- Add all included snippets to the
  [Wiki](https://github.com/rafamadriz/friendly-snippets/wiki).

## Thanks to all contributors

<a href="https://github.com/rafamadriz/friendly-snippets/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=rafamadriz/friendly-snippets" />
</a>

## Credits

A good portion of the snippets have been forked from the following repositories:

- [vscode-standardjs-snippets](https://github.com/capaj/vscode-standardjs-snippets)
- [python-snippets](https://github.com/cstrap/python-snippets)
- [vs-snippets](https://github.com/kitagry/vs-snippets)
- [Wscats/html-snippets](https://github.com/Wscats/html-snippets)
- [Harry-Ross/vscode-c-snippets](https://github.com/Harry-Ross/vscode-c-snippets)
- [vscode-jekyll-snippets](https://github.com/edheltzel/vscode-jekyll-snippets)
- [vscode-fortran-support](https://github.com/krvajal/vscode-fortran-support)
- [vscode_cobol](https://github.com/spgennard/vscode_cobol)
- [VSCode-LaTeX-Snippets](https://github.com/JeffersonQin/VSCode-LaTeX-Snippets)
- [vscode-react-javascript-snippets](https://github.com/dsznajder/vscode-react-javascript-snippets)
- [honza/vim-snippets - Verilog](https://github.com/honza/vim-snippets/blob/master/snippets/verilog.snippets)
- [vscode-relm4-snippets](https://github.com/Relm4/vscode-relm4-snippets)
- And more...
