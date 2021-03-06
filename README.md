# nvim-ts-rainbow
Rainbow parens for neovim using tree-sitter. Needs [nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter).

Tested languages - lua, java, clojure, fennel, python, css. Should work with any language, except bash and idk probably something else too.

(**Update** - lua works after [neovim/neovim/#133357](https://github.com/neovim/neovim/pull/13357) was merged)

## Setup
```lua
require'nvim-treesitter.configs'.setup {
  rainbow = {
    enable = true,
    disable = {'bash'} -- please disable bash until I figure #1 out
  }
}
```

### Colours
I've used the gruvbox palette because it is nice and subtle. I wanted to use VIBGYOR for an actual rainbow, but
 - indigo and blue look the same.
 - the colours were too bright and distracting.

To change the colours, edit `lua/rainbow/colors.lua`. If you want to override only a *few* colours (you can only change colours 1 through 7 this way), you can do it in your init.vim: (thanks @delphinus !)
```vim
hi rainbowcol1 guifg=#123456
```
## Screenshots
![alt text](https://raw.githubusercontent.com/p00f/nvim-ts-rainbow/master/screenshots/java.png)
![alt text](https://raw.githubusercontent.com/p00f/nvim-ts-rainbow/master/screenshots/clojure.png)
![alt text](https://raw.githubusercontent.com/p00f/nvim-ts-rainbow/master/screenshots/fennel.png)
## Credits
Huge thanks to @vigoux, @theHamsta, @sogaiu and @steelsojka for all their help
