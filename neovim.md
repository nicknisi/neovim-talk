autoscale: true

# neovim

![](http://www.officialpsds.com/images/thumbs/The-Matrix-Neo-psd31090.png)

---

# [fit] What's wrong with vim?

* Nothing!
* over 20 years old
* 300K lines of "scary" C89 code
* All code is Bram Mooleaner's responsibility
* Lots of platform-specific code
* All plugin code runs synchronously

![left filtered](https://irishyouthphilosophy.files.wordpress.com/2012/08/morpheus-pill.png)

---

# [fit] What does neovim do better?

![](http://justinwise.net/wp-content/uploads/2012/10/neo-matrix-there-is-no-spoon-555x306.png)

* Aggressively refactor source code[^1]
	* Replace platform-specific code with libuv
	* Simplify maintenance
* Split work between multiple developers
* Provide a new plugin architecture based on coprocesses
	* Plugins can be written in any language without explicit support from the editor

[^1]: https://github.com/neovim/neovim/wiki/Introduction

---

# Installing neovim

*OSX*

```bash
brew tap neovim/neovim
brew install --HEAD neovim
```

*Ubuntu*

```bash
sudo add-apt-repository ppa:neovim-ppa/unstable
sudo apt-get update
sudo apt-get install neovim
```

*Windows (experimental)*

See https://github.com/neovim/neovim/wiki/Installing-Neovim#windows

---

# What else do I need to do to get started?

---

# `nvim`

![](http://img02.deviantart.net/1894/i/2006/033/2/c/matrix_code_by_phi_au.jpg)

---

# There be dragons

![inline](https://d1zjcuqflbd5k.cloudfront.net/files/acc_154831/19PMI?response-content-disposition=inline;%20filename=Screen%20Shot%202015-10-08%20at%2017.34.41.png&Expires=1444343991&Signature=EyFRo7n7bhevfouTPGlxrqZei7oRIRzkua9mKLFNY0hOU~gcyIuJZSG33CIk6dFG2COBdqLS3a8vyklcVUYP2xGle9ackiMYwVIQ8rHt-c4r0d6qnWvG0dXjz0GV6w7OSjNEEr5UURjPOYLY34XpDNBqFpBLqPO~quik4fE~BYs_&Key-Pair-Id=APKAJTEIOJM3LSMN33SA)

---

# [fit] But I alread have a very complicated `.vimrc`

```bash
ln -s ~/.vimrc ~/.nvimrc
ln -s ~/.vim ~/.nvim
alias vim="nvim"
```

---

# Did you notice a difference?
#### me either

---

# Let's make a few _small_ changes
![230%](http://vignette4.wikia.nocookie.net/matrix/images/f/fb/Architect.png)

---

# [fit] Syntastic -> Neomake

---

# Syntastic and Neomake

![left filtered](http://www.eds-online.net/designs/matrix/images/twins.png)

* Syntax checking plugin for vim/neovim
* Runs files through an external syntax checker and displays the resulting errors on file save
* JSHint
* TSLint
* Rubocop

---

# vim-plug

![](http://cdn3.politicaloutcast.com/wp-content/uploads/2014/10/matrix-baby.jpg)

--- 

# vim-plug

Similar to vundle, but super-fast!

```vim
call plug#begin('~/.vim/plugged')

Plug 'tpope/vim-fugitive'
Plug 'tpope/vim-repeat'
Plug 'garbas/vim-snipmate'

" On-demand loading
Plug 'scrooloose/nerdtree', { 'on':  'NERDTreeToggle' }

" Unmanaged plugin (manually installed and updated)
Plug '~/my-prototype-plugin'

" Add plugins to &runtimepath
call plug#end()
```

---

# There's more!

![](http://digital-art-gallery.com/oid/29/1023x553_6604_APU_Matrix_3d_mech_sci_fi_robot_picture_image_digital_art.jpg)

---

# `:terminal`

Open a terminal in a neovim buffer

![inline](https://d1zjcuqflbd5k.cloudfront.net/files/acc_154831/1eVOB?response-content-disposition=inline;%20filename=Screen%20Shot%202015-10-08%20at%205.28.16%20PM.png&Expires=1444343618&Signature=dzym70KRYifBoeg4XLuksBo6gB-ZuDQs0R08moogPFHj8KUBI25IjTXMZyAleB9nS3-ATZjv~mj3tsKBvi5ceYIYuErEuVXIYzy~d4~KRlOmz5QH49ABX5IjfFah46durLv6JDJ~A1QyN~y1ADpOibK4Bn0w1Zn6B1VEj12Msdo_&Key-Pair-Id=APKAJTEIOJM3LSMN33SA)

---

# Looks cool!

![530%](http://geekychristian.com/wp-content/uploads/2013/12/Neo-thumb-pete-A.jpg)

---

# @nicknisi

![](http://nicknisi.com/images/beef_nick.png)

