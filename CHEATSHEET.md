# Neovim Cheatsheet

This config is based on Kickstart.nvim. The leader key is `Space`.

Sources:
- Main config: `init.lua`
- Neo-tree config: `lua/kickstart/plugins/neo-tree.lua`
- Installed plugin lockfile: `lazy-lock.json`

## Essentials

| Shortcut | Mode | Action |
| --- | --- | --- |
| `<Esc>` | Normal | Clear search highlight |
| `<Space>q` | Normal | Open diagnostics in the location list |
| `<Esc><Esc>` | Terminal | Exit terminal mode |
| `<C-h>` | Normal | Move to left split |
| `<C-j>` | Normal | Move to lower split |
| `<C-k>` | Normal | Move to upper split |
| `<C-l>` | Normal | Move to right split |
| Arrow keys | Normal | Disabled; use `h`, `j`, `k`, `l` |

## Window Splits

| Action | Command | Shortcut |
| --- | --- | --- |
| Horizontal split | `:split` or `:sp` | `Ctrl-w s` |
| Vertical split | `:vsplit` or `:vs` | `Ctrl-w v` |
| Open file in horizontal split | `:sp path/to/file` | - |
| Open file in vertical split | `:vs path/to/file` | - |
| Next window | - | `Ctrl-w w` |
| Move left | - | `Ctrl-w h` |
| Move down | - | `Ctrl-w j` |
| Move up | - | `Ctrl-w k` |
| Move right | - | `Ctrl-w l` |
| Close current window | `:q` | `Ctrl-w q` |
| Close all other windows | `:only` | - |

## Tabs

| Action | Command | Shortcut |
| --- | --- | --- |
| Next tab | `:tabnext` | `gt` |
| Previous tab | `:tabprevious` | `gT` |
| Go to tab 2 | - | `2gt` |
| First tab | `:tabfirst` | - |
| Last tab | `:tablast` | - |
| New empty tab | `:tabnew` | - |
| Open file in new tab | `:tabnew path/to/file` | - |
| Close current tab | `:tabclose` | - |

## Neo-tree

| Shortcut | Where | Action |
| --- | --- | --- |
| `\` | Normal | Reveal current file in Neo-tree |
| `\` | Neo-tree | Close Neo-tree window |
| `?` | Neo-tree | Show Neo-tree help and mappings |
| `<Enter>` | Neo-tree | Open file or expand/collapse directory |
| `<Space>` | Neo-tree | Toggle directory node |
| `S` | Neo-tree | Open in horizontal split |
| `s` | Neo-tree | Open in vertical split |
| `t` | Neo-tree | Open in new tab |
| `w` | Neo-tree | Open with window picker |
| `P` | Neo-tree | Toggle preview |
| `<C-f>` | Neo-tree | Scroll preview down |
| `<C-b>` | Neo-tree | Scroll preview up |
| `C` | Neo-tree | Close node |
| `z` | Neo-tree | Close all nodes |
| `R` | Neo-tree | Refresh |
| `a` | Neo-tree | Add file or directory |
| `A` | Neo-tree | Add directory |
| `d` | Neo-tree | Delete file or directory |
| `r` | Neo-tree | Rename file or directory |
| `b` | Neo-tree | Rename basename only |
| `y` | Neo-tree | Copy to Neo-tree clipboard |
| `x` | Neo-tree | Cut to Neo-tree clipboard |
| `p` | Neo-tree | Paste from Neo-tree clipboard |
| `<C-r>` | Neo-tree | Clear Neo-tree clipboard |
| `c` | Neo-tree | Copy to typed destination |
| `m` | Neo-tree | Move to typed destination |
| `e` | Neo-tree | Toggle auto-expand width |
| `q` | Neo-tree | Close window |
| `<` | Neo-tree | Previous source |
| `>` | Neo-tree | Next source |

### Neo-tree Filesystem

| Shortcut | Action |
| --- | --- |
| `H` | Toggle hidden files |
| `/` | Fuzzy find in tree |
| `D` | Fuzzy find directory |
| `#` | Fuzzy sort |
| `f` | Filter on submit |
| `<C-x>` | Clear filter |
| `<Backspace>` | Navigate up |
| `.` | Set root to selected directory |
| `[g` | Previous git-modified item |
| `]g` | Next git-modified item |
| `i` | Show file details |
| `o` | Show order-by help |
| `oc` | Order by created time |
| `od` | Order by diagnostics |
| `og` | Order by git status |
| `om` | Order by modified time |
| `on` | Order by name |
| `os` | Order by size |
| `ot` | Order by type |

## Telescope Search

| Shortcut | Mode | Action |
| --- | --- | --- |
| `<Space>sh` | Normal | Search help |
| `<Space>sk` | Normal | Search keymaps |
| `<Space>sf` | Normal | Search files |
| `<Space>ss` | Normal | Search Telescope builtins |
| `<Space>sw` | Normal/Visual | Search word or visual selection |
| `<Space>sg` | Normal | Live grep |
| `<Space>sd` | Normal | Search diagnostics |
| `<Space>sr` | Normal | Resume previous Telescope picker |
| `<Space>s.` | Normal | Search recent files |
| `<Space>sc` | Normal | Search commands |
| `<Space><Space>` | Normal | Search open buffers |
| `<Space>/` | Normal | Fuzzy search current buffer |
| `<Space>s/` | Normal | Live grep in open files |
| `<Space>sn` | Normal | Search Neovim config files |

Inside Telescope, use `<C-/>` in insert mode or `?` in normal mode to show picker-specific shortcuts.

## LSP

These mappings exist only in buffers where an LSP server is attached.

| Shortcut | Mode | Action |
| --- | --- | --- |
| `grn` | Normal | Rename symbol |
| `gra` | Normal/Visual | Code action |
| `grr` | Normal | References |
| `gri` | Normal | Implementation |
| `grd` | Normal | Definition |
| `grD` | Normal | Declaration |
| `gO` | Normal | Document symbols |
| `gW` | Normal | Workspace symbols |
| `grt` | Normal | Type definition |
| `<Space>th` | Normal | Toggle inlay hints, if supported |

Configured LSP/tool installs:
- `pylsp`
- `lua_ls`
- `stylua`

## Formatting And Completion

| Shortcut | Mode | Action |
| --- | --- | --- |
| `<Space>f` | Normal/Visual | Format buffer or selection with Conform |
| `<C-y>` | Insert | Accept completion |
| `<Tab>` / `<S-Tab>` | Insert | Move through snippet placeholders |
| `<C-Space>` | Insert | Open completion menu or docs |
| `<C-n>` / `<C-p>` | Insert | Select next/previous completion item |
| `<Up>` / `<Down>` | Insert | Select previous/next completion item |
| `<C-e>` | Insert | Hide completion menu |
| `<C-k>` | Insert | Toggle signature help |

Completion sources:
- LSP
- Paths
- Snippets

## Mini.nvim Helpers

Active Mini modules:
- `mini.ai` for improved around/inside text objects
- `mini.surround` for add/delete/replace surroundings
- `mini.statusline` for the statusline

Useful examples from the config:

| Example | Action |
| --- | --- |
| `va)` | Visually select around parentheses |
| `yinq` | Yank inside next quote |
| `ci'` | Change inside single quotes |
| `saiw)` | Add parentheses around inner word |
| `sd'` | Delete surrounding single quotes |
| `sr)'` | Replace surrounding parentheses with single quotes |

## Git

`gitsigns.nvim` is active and shows git signs in the gutter.

The extra gitsigns shortcut module at `lua/kickstart/plugins/gitsigns.lua` is currently commented out in `init.lua`, so these common hunk shortcuts are not active unless that module is enabled.

## Active Plugins

| Plugin | Purpose |
| --- | --- |
| `folke/lazy.nvim` | Plugin manager |
| `NMAC427/guess-indent.nvim` | Detect indentation settings |
| `lewis6991/gitsigns.nvim` | Git signs in the gutter |
| `folke/which-key.nvim` | Show available keymaps as you type |
| `nvim-telescope/telescope.nvim` | Fuzzy finder and picker UI |
| `nvim-telescope/telescope-fzf-native.nvim` | Faster Telescope sorter |
| `nvim-telescope/telescope-ui-select.nvim` | Use Telescope for `vim.ui.select` |
| `nvim-lua/plenary.nvim` | Lua utility dependency |
| `nvim-tree/nvim-web-devicons` | File icons |
| `neovim/nvim-lspconfig` | LSP client configuration |
| `mason-org/mason.nvim` | External tool installer UI |
| `mason-org/mason-lspconfig.nvim` | Mason integration for LSP servers |
| `WhoIsSethDaniel/mason-tool-installer.nvim` | Auto-install configured tools |
| `j-hui/fidget.nvim` | LSP progress/status notifications |
| `stevearc/conform.nvim` | Formatting |
| `saghen/blink.cmp` | Completion engine |
| `L3MON4D3/LuaSnip` | Snippet engine |
| `folke/tokyonight.nvim` | Colorscheme |
| `folke/todo-comments.nvim` | Highlight TODO/FIXME-style comments |
| `nvim-mini/mini.nvim` | Small editor utilities |
| `nvim-treesitter/nvim-treesitter` | Treesitter syntax, highlighting, indentation |
| `nvim-neo-tree/neo-tree.nvim` | File explorer |
| `MunifTanjim/nui.nvim` | UI dependency for Neo-tree |

## Installed But Not Enabled In This Config

These example modules exist under `lua/kickstart/plugins/`, but their `require` lines are currently commented out in `init.lua`.

| Module | Plugin(s) |
| --- | --- |
| `kickstart.plugins.debug` | `mfussenegger/nvim-dap`, `rcarriga/nvim-dap-ui`, `nvim-neotest/nvim-nio`, `jay-babu/mason-nvim-dap.nvim`, `leoluz/nvim-dap-go` |
| `kickstart.plugins.indent_line` | `lukas-reineke/indent-blankline.nvim` |
| `kickstart.plugins.lint` | `mfussenegger/nvim-lint` |
| `kickstart.plugins.autopairs` | `windwp/nvim-autopairs` |
| `kickstart.plugins.gitsigns` | Adds recommended keymaps for the already-active `gitsigns.nvim` plugin |

The custom plugin import `{ import = 'custom.plugins' }` is also commented out, and `lua/custom/plugins/init.lua` currently returns an empty plugin list.
