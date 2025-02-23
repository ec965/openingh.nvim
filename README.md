# openingh.nvim
Opens the current file or project page in GitHub.

![Lua](https://img.shields.io/badge/Made%20with%20Lua-blueviolet.svg?style=for-the-badge&logo=lua) [![lint with luacheck](https://img.shields.io/github/workflow/status/gbprod/yanky.nvim/Integration?style=for-the-badge)](https://github.com/Almo7aya/openingh.nvim/actions/workflows/lint.yml)


  - Features
    - Supports MacOS, Linux, and maybe Windows 🤷‍♂️
    - Works with detached HEAD and supports checked out branches or forks
    - Automatically selects the correct line number in the file page 

  - Demo

![](./gifs/demo.gif)

## Requirements

  - Neovim 0.7.2+

## Installation

#### Example with Packer

[wbthomason/packer.nvim](https://github.com/wbthomason/packer.nvim)

```lua
-- init.lua
require("packer").startup(function()
  use "almo7aya/openingh.nvim"
end)
```

## Commands

- `:OpenInGHRepo`
  - Opens the project's git repository page in GitHub.

- `:OpenInGHFile`
  - Opens the current file page in GitHub.

## Usage

You can call the commands directly or define mappings them:

```lua
-- for repository page
vim.api.nvim_set_keymap("n", "<Leader>gr", ":OpenInGHRepo <CR>", { expr = true, noremap = true })

-- for current file page
vim.api.nvim_set_keymap("n", "<Leader>gf", ":OpenInGHFile <CR>", { expr = true, noremap = true })
```

## TODO

  - [x] Support the current file cursor position
  - [ ] Support visual mode to open a file in range selection 
  - [ ] Support support other version control websites 

## Contribution

Feel free to open an issue or a pull request if you have any suggestion or improvements 

## License

[MIT](./LICENSE)

