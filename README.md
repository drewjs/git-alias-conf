# Git Alias Configuration

A helpful list of commands for your git workflow.

More information: [Ultimate Git Alias Setup](http://durdn.com/blog/2012/11/22/must-have-git-aliases-advanced-examples/)

## Installation

Add the following section to `~/.gitconfig`:
``` bash
[alias]
        # inspection
        ls = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate
        ll = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --numstat
        lds = log --pretty=format:"%C(yellow)%h\\ %ad%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --date=short
        ld = log --pretty=format:"%C(yellow)%h\\ %ad%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --date=relative
        fl = log -u
        dl = !git ll -1
        dlc = diff --cached HEAD^
        f = !git ls-files | grep -i

        # view aliases
        la = !git config -l | grep alias | cut -c 7-

        # point of no return
        rh = reset --hard HEAD
        rh1 = reset --hard HEAD^
        rh2 = reset --hard HEAD^^
```


