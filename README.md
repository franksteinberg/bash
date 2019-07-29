# Custom Bash Config
Original config from: https://github.com/jaivardhankapoor/bestbash

###Functions
Custom commands for super lazy people ;)

1. up:go up the directory structure specified number of times
1. extract: Extracts zip, tar.gz,tar.bz2 files in one command
1. compress: similar to above
1. to_iso: Converts to ISO
1. remindme: uses notify-send to display notification after specified number of time(remindme [time in seconds] [text])
1. calc: a simple calculator
1. ff: find file with a pattern in name
1. fe: find file with pattern in name and execute a command on it(example: fe a.out 1)
1. lowercase: move filenames to lowercase
1. swap: swap2 filenames around
1. dirsize: Self explanatory
1. fared: find and remove all empty directories

##Configuration Instructions
  ```
  #clone into home
  git clone https://github.com/franksteinberg/bash ~/.bash/
  #backup old .bashrc and .bashrc related files
  mv .bashrc .bashrc.bak
  #create symlink for .bashrc
  ln -s ~/.bash/init ~/.bashrc
  #ALL DONE!
 ```
 
 ## Making Changes to aliases
1. If you make changes to any of the files, just type `sa` to source aliases
 * It actually sources `.bashrc`, but I am used to typing `ea` and `sa` to edit/source my aliases.
1. The bash prompt is defined in `.bash/colors` - Edit this file to change the prompt to your liking
 * It was easiest to just leave this here from the original repo I forked because it references colors defined in this file.
 * It is currently configured to display your current git branch, the time, the user@hostname, and the current directory.

## NOTE FOR MAC USERS:
If you are on a Mac, by default, you may have a `.bash_profile` instead of a `.bashrc`. If you do not have a `.bashrc`, create the symlink for `.bashrc` to `.bash/init` as described in the Configuration Instructions above, however make sure to also include this step:

1. Edit your `~/.bash_profile` and add the following lines:
```
# Source .bashrc
if [ -f ~/.bashrc ]; then
    . ~/.bashrc
fi
```
