DOT-VIM REPOSITORY
==================


Description
-----------

This repo is for my .vim directory.
It contains my .vimrc and the plugins/scripts I use.
The plugins are installed with Pathogen to allow easy updating via git.


Credit
------

I learned this technique from vimcasts.org
A full screencast and article is available from here:
http://vimcasts.org/episodes/synchronizing-plugins-with-git-submodules-and-pathogen/


To add a new plugin from Github (preferred)
-------------------------------------------

    cd ~/.vim
    git submodule add http://github.com/tpope/vim-fugitive.git bundle/fugitive
    git add .
    git commit -m "Install \"Fugitive\" bundle as a submodule."
    git push


To install this repo on a new machine
-------------------------------------

    git clone git@github.com:stevenocchipinti/dotvim.git ~/.vim
    ln -s ~/.vim/vimrc ~/.vimrc
    ln -s ~/.vim/gvimrc ~/.gvimrc
    cd ~/.vim
    git submodule update --init


To update one submodule
-----------------------

    cd ~/.vim/bundle/fugitive
    git pull origin master


To update all submodules
------------------------

    cd ~/.vim
    git submodule foreach git pull origin master