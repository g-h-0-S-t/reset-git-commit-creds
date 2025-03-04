# reset-git-commits-and-creds

Want to reset entire git history and creds?  
Exposed your private / personal info by mistake in your commit messages or email id?  
Here's how you can do it

```
git checkout --orphan temp && git add -A && GIT_AUTHOR_EMAIL="<git no-reply email>" GIT_COMMITTER_EMAIL="<git no-reply email>" git commit -m "init" && git branch -D main && git branch -m main && git config pull.rebase false && git push -f --set-upstream origin main
```
