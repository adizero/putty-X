* Improved support of ctrl-shift-alt modifiers and F1-F12 function keys.

* Italics support in terminal.

* Many other improvements.

Forked from PuTTY 0.62.

Compile with mingw.

For example use this Arch based docker with installed mingw [docker-mingw-arch] (https://github.com/mdimura/docker-mingw-arch)

    git clone https://github.com/mdimura/docker-mingw-arch
    cd docker-mingw-arch
    docker build -t docker-mingw-arch .
    docker run -it docker-mingw-arch bash

    # within docker (svn is needed only for kitty compilation, not putty)
    yay -S iputils vim svn

    # checkout and build putty-X
    git clone https://github.com/adizero/putty-X
    cd putty-X/windows
    make -f Makefile.cyg

If only putty.exe is needed: `make -f Makefile.cyg putty.exe`
