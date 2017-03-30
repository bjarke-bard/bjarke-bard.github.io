+++
date = "2017-03-24T11:56:33+01:00"
title = "Checkout Subdirectory"
draft = false

+++

When you don't want the whole repo you can with "core.sparsecheckout" checkout only part of a repo.

<!--more-->
```bash
mkdir <repo> && cd <repo>

git init

git remote add –f origin <url>

git config core.sparsecheckout true

echo some/dir/ >> .git/info/sparse-checkout

git pull <remote> <branch>

git read-tree -mu HEAD
```
http://jasonkarns.com/blog/subdirectory-checkouts-with-git-sparse-checkout/
