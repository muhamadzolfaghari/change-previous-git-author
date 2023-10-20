# change-previous-git-author
This code allows to change author details such as name and email and rebase that with new details.

To change the author of a previous Git commit, you can use the git rebase command. Here are the steps:

First, if you haven’t already done so, you will likely want to fix your name in git-config:

```shell
git config --global user.name "<author name>"
git config --global user.email "<author email>"
```

Second, to rewrite metadata for a range of commits using a rebase, do the following:
```shell
git rebase -r <commit id> --exec 'git commit --amend --no-edit --reset-author'
```
