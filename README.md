# Vim Cheatsheet

This is a "cheat sheet" of Vim commands I curently know and use:

<h3>Basic Commands</h3>

Command | Description | Hint
------------ | ------------- | -------------
`Esc` | normal mode | if you are unsure about something you typed
`Ctrl+g` | show location in file and the file status |
`Ctrl+o` | go back where you came from |
`Ctrl+i` | go forward where you came from |
`Ctrl+w Ctrl+w` | jump from one window to another |
`Ctrl+d` | when in `:` mode in order for Vim to show a list of commands | `<TAB>` will complete the name

<h3>Moving in Vim</h3>

Command | Description | Hint
------------ | ------------- | -------------
`h` `left arrow` | move the cursor to the left | the `h` key is at the left and moves left
`j` `down arrow` | move the cursor down | the `j` key looks like a down arror
`k` `up arrow` | move the cursor up |
`l` `right arrow` | move the cursor to the right | the `l` key is a the right and moves right
`w` | move the cursor one word forward | `#w` move cursor # words forward <br>`#` can be any number
`e` | move the cursor to the end of the word | `#e` move cursor at the end of # words <br>`#` can be any number
`0` | move the cursor to the start of the line |
`$` | move the cursor to the end of the line |
`G` | move to the bottom of the file | `#G` move to the line number in the file <br>`#` can be any line number
`gg` | move to the start of the file |

<h3>Exiting Vim</h3>

Command | Description | Hint
------------ | ------------- | -------------
`:q` | exit editor | if there are no changes made
`:q!` | exit editor, discard changes | `q` stands for quit and `!` stands for dicard changes
`:wq` | exit editor, save changes | `w` stands for write and `q` stands for quit

<h3>Text Editing</h3>

Command | Description | Hint
------------ | ------------- | -------------
`x` | delete a character | after the cursor
`i` | insert text | before the cursor <br>`Esc` to return to normal mode
`a` | append text | after the cursor <br>`Esc` to return to normal mode
`A` | append text | after the line <br>`Esc` to return to normal mode
`dw` | delete a word until the start of the next word | `d#w` to delete # words, `#` can be replaced with any number
`de` | delete a word to the end of the current word | `d#e` to delete # words, `#` can be replaced with any number
`d$` | delete line | after the cursor to the end of last character
`dd` | delete a whole line | `#dd` delete # whole lines, `#`  can be replaced with any number
`u` | undo the last command | `U` to fix the whole line
`Ctrl+r` | redo the last undo |
`p` | put previously deleted or copyied text after the cursor | `p` stands for paste
`r` | replace the character under the cursor | `R` replace multiple characters under the cursor
`c` | change from the cursor to where the motion takes you | `ce` change end <br>`cw` change word <br>`c$` change line
`o` | open a line bellow the cursor | `O` open a line above the cursor
`v` | start visual selection | `y` copy the selected text <br>`x` cut the selected text <br>`p` paste the selected text <br>`d` delete the selected text


<h3>Search Select and Replace in File</h3>

Command | Description | Hint
------------ | ------------- | -------------
`/word` | search forwards for word or phrase |
`?word` | search backwards for word or phrase |
`n` | search again in forwards direction |
`N` | search agasin in backwards direction |
`%` | find matching paranthesis or bracket |
`:s/old/new` | substitute `old` word with `new` word in the current line |
`:s/old/new/g` | substitute every occurence in the whole line |
`:#,#s/old/new/g` | substitute `old` word with `new` word in # lines | `#` can be any line number
`:%s/old/new/g` | substitute every occurence in the whole file |
`:%s/old/new/gc` | find every occurence in the whole file with a prompt <br>whether to substittute or not | `c` stands for confirmation

<h3>Set Options</h3>

Command | Description | Hint
------------ | ------------- | -------------
`:set ic` `ignorecase` | set ignore case for search | `/word\c` set ignore case for just one search
`:set noic` `noignorecase` | disable ignoring case | ignore upper/lower case when searching
`:set hls` `hlsearch` | set highlight search | highlight all matching phrases
`:set nohls` nohlsearch` | disable highlight search |
`:set is` `incsearch` | set incremental search | show partial matches for a search phrase
`:set nois` noincsearch` | disable incremental search |

<h3>External Commands</h3>

Command | Description | Hint
------------ | ------------- | -------------
`:!ls` | list files in current directory |
`:w fileName` | save the current Vim file to disk with the name fileName | `w` stands for write
`!rm fileName` | delete fileName file | `rm` stands for remove
`v :w fileName` | write the Visually selected lines in fileName |
`:r fileName` | paste text from file fileName bellow the cursor position | `r` stands for retrieve 
`:r !ls` | retrieve output of the ls command and paste it bellow the cursor position |

<h3>Getting Help</h3>

Command | Description | Hint
------------ | ------------- | -------------
`:help` | open Vim comprehensive on-line help system |
`:help command` | find help on just about any subject | `command` can be any command
`:help user-manual` | open Vim user manual |
`:help insert-index` | open Vim insert index |
`:help vimrc-intro` | open vimrc help file |
`:help cmd` | open vim help file on command |
