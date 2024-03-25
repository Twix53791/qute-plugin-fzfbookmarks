# qute-plugin-fzfbookmarks
Manage your bookmarks with fzf in a popup window. Add bookmarks, categories, rename and delete entries.

## Installation

```
git clone https://github.com/Twix53791/qute-plugin-fzfbookmarks/
cd qute-plugin-fzfbookmarks
cp fzfbookmarks-userscript ~/.config/qutebrowser/userscripts/
cp qute-plugin-fzfbookmarks ~/config/qutebrowser/bin/
```

* **edit `fzfbookmarks-userscript` to fit your config. I use for example `kitty` as a terminal, but maybe not you...**
* `qute-plugin-fzfbookmarks` can be copied in any bin path, for example /usr/local/bin. I have created a bin folder in qutebrowser config I added to my bin path in .zshrc (or .bashrc), but you can use your own setup.

## Use
In `config.py`:
```
'b': 'spawn -u fzfbookmarks-userscript list',
'B': 'spawn -u fzfbookmarks-userscript add',
'<ctrl-b>': ':set-cmd-text -s :spawn -u fzfbookmarks-userscript quickadd',
```

### Structure
`fzfbookmarks-userscript` run a termminal window (I recommand to make it floating for example in your window manager rules), running the command `qute-plugin-fzfbookmarks` which displays the content of `$QUTE_CONFIG_DIR/bookmarks/bookmarks`

