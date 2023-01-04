# How to get the Linux tools for Git for Windows?

1. Download [MSYS2](https://www.msys2.org/) .
2. Open MSYS2, use `pacman -S tmux` or `pacman -S zsh` (or whatever you want) to install, but make sure you just install one tool at once.
3.  Use [7-Zip-zstd](https://github.com/mcmilk/7-Zip-zstd/releases) to decompress `.zst` files in `msys64\var\cache\pacman\pkg`, you will get `.tar` files.
4. Decompress the `.tar` files you will get  `usr`, `etc` and other folders or files, just cut thesefolders or files directly into the `Git\` directory.

## Tmux for Git for Windows

Contains:

+ tmux-3.3.a-1-x86_64
+ libevent-2.1.12-3-x86_64 

The tmux repository is [here](https://github.com/tmux/tmux).

## ZSH for Git for Windows

Contains:

+ zsh-5.9-2
+ pcre-8.45-3
+ libpcre16-8.45-3
+ libpcre32-8.45-3
+ libpcrecpp-8.45-3
+ libpcreposix-8.45-3

The zsh repository is [here](https://sourceforge.net/p/zsh/code/ci/master/tree/).

### Replace default Bash with  ZSH

Under the current user folder, find or create a `.bashrc` file, paste the following content into the configuration file, and set the default shell to ZSH:

```bash
# # Launch Zsh
if [ -t 1 ]; then
exec zsh
fi
```

But I have to warn you, most plugins for ZSH are made for Linux, you can try them in Windows.

# License

The licenses of these tools above are the same as the original projects. If my idea is helpful to you, please indicate the source.

CC BY-NC-SA 4.0
