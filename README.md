# Bluloco.nvim

A fancy but yet sophisticated light and dark designer neovim theme built with [lush.nvim](https://github.com/rktjmp/lush.nvim).
It features a much more comprehensive usage of syntax scopes and color
consistency, with due regards to aesthetics, contrast and readability.
Most popular plugins are also supported, see [Plugins](#plugins)


## Install

Install Bluloco with your favorite package manager.

### [packer](https://github.com/wbthomason/packer.nvim)

```lua
use {
    'paponahmedsharad/bluloco.nvim',
    requires = { 'rktjmp/lush.nvim' }
}
```

### [lazy.nvim](https://github.com/folke/lazy.nvim)

```lua
{
  'paponahmedsharad/bluloco.nvim',
  lazy = false,
  priority = 1000,
  dependencies = { 'rktjmp/lush.nvim' },
  config = function()
    -- your optional config goes here, see below.
  end,
},
```

## Usage

> ⚠️ The `setup()` function is optional but please call it
> **before** you set the colorscheme if you want to adjust the config.

These are the default values:

```lua
require("bluloco").setup({
  style = "auto"               -- "auto" | "dark" | "light"
  transparent = false,
  italics = false,
  terminal = vim.fn.has("gui_running") == 1 -- bluoco colors are enabled in gui terminals per default.
})

vim.cmd('colorscheme bluloco')
```

You can also apply the style variant directly.
These are especially helpful when switching in an already running vim session.

```vim
:colorscheme bluloco-dark
:colorscheme bluloco-light
```

#### Lualine

Make sure your lualine settings are set to auto:

```lua
require('lualine').setup {
  options = {
    theme = 'auto'
  }
}
```
