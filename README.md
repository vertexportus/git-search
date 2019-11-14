# git-search
git search command extension for helping to search for, and work with, branches

## requirements

for clipboard features, `xclip` is needed

## usage

have git-search script in a folder set in PATH
all searches use a `<value>` parameter to match branches. If a single branch is found it's automatically selected, if more than one is found, the script displays all found as a numbered list, and inputting the number will select that branch.

By default it searches LOCAL branches only, but accepts the `-o` or `--origin` parameter to search remote branches as well

`git search <value>`

 copies selected branch to clipboard

`git search -b <value>`

 does a `git checkout` of selected branch (also accepts as `--branch`)
 use `-p` or `--pull` to also pull selected branch after checkout

`git search -m <value>`

 does a `git merge` of selected branch into CURRENT branch (also accepts as `--merge`)
 use `-p` or `--pull` to pull selected branch BEFORE merge

 the command will display the names of the branches being merged, and asks for confirmation
 