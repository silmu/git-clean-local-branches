# Git commands for deleting branches that no longer exist

Delete all local branches that no longer exist in remote:
```
git fetch -p && git branch -vv | awk '/: gone]/{print $1}' | xargs git branch -d
```    
Delete local branch:
```
git branch --delete <branchname>
```
