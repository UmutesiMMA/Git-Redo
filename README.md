# Git-Redo

## Bundle1
### exercise 1
```bash
user@DESKTOP-TQVNUUS MINGW64 ~
$ cd ~/Documents/TheGym2/Git/

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git
$ git init
Initialized empty Git repository in C:/Users/user/Documents/TheGym2/Git/.git/

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (master)
$ git branch -m master main

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ touch index.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ touch style.css

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ touch begin.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git mv begin.html start.html
fatal: not under version control, source=begin.html, destination=start.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git add .

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git commit -m "first"
[main (root-commit) c50afc4] first
 3 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html
 create mode 100644 start.html
 create mode 100644 style.css

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git remote add origin https://github.com/UmutesiMMA/Git-Redo.git
user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 229 bytes | 57.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/UmutesiMMA/Git-Redo.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git branch dev

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git branch
  dev
* main

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git checkout dev
Switched to branch 'dev'
user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (dev)
$ git checkout -b test
Switched to a new branch 'test'

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (test)
$ git checkout dev
Switched to branch 'dev'

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (dev)
$ git branch -d test
Deleted branch test (was c50afc4).

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (dev)
$ git push --set-upstream origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/UmutesiMMA/Git-Redo/pull/new/dev
remote:
To https://github.com/UmutesiMMA/Git-Redo.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.
```
### Exercise2
```bash
user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (dev)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ touch home.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash
No local changes to save

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git add .

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash "home page"
fatal: subcommand wasn't specified; 'push' can't be assumed due to unexpected token
'home page'

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash
Saved working directory and index state WIP on main: c50afc4 first

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ touch about.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git add about.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash
Saved working directory and index state WIP on main: c50afc4 first

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ touch team.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git add .

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash
Saved working directory and index state WIP on main: c50afc4 first

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash list
stash@{0}: WIP on main: c50afc4 first
stash@{1}: WIP on main: c50afc4 first
stash@{2}: WIP on main: c50afc4 first

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash show stash@{2}
 home.html | 13 +++++++++++++
 1 file changed, 13 insertions(+)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash show stash@{1}
 about.html | 15 +++++++++++++++
 1 file changed, 15 insertions(+)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (6f71fcb5c3ffbc79172bfcfc6f2e8ac19a1c9778)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash list
stash@{0}: WIP on main: c50afc4 first
stash@{1}: WIP on main: c50afc4 first

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (1ab7f77cc6f7a3827c493793c67048415a0ca0da)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git commit -m "about and home page"
[main 81b8c35] about and home page
 2 files changed, 28 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 927 bytes | 463.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/UmutesiMMA/Git-Redo.git
   c50afc4..81b8c35  main -> main

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash list
stash@{0}: WIP on main: c50afc4 first

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (1892370a00076e7ad79e924113aecf6ff9bdd2f1)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git log
commit 81b8c35073cb40d5fa81234d69ddd635229f26bd (HEAD -> main, origin/main)
Author: umutesimagnificat@gmail.com <umutesimagnificat@gmail.com>
Date:   Tue Jul 11 12:01:14 2023 +0200

    about and home page

commit c50afc4634cc26ba8c97a63299163c143daf64f7 (origin/dev, dev)
Author: umutesimagnificat@gmail.com <umutesimagnificat@gmail.com>
Date:   Tue Jul 11 11:15:24 2023 +0200

    first

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git reset 81b8c35073cb40d5fa81234d69ddd635229f26bd

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$
```
## BUNDLE2
### Exercise1
```bash

user@DESKTOP-TQVNUUS MINGW64 ~
$ cd ~/Documents/TheGym2/Git/

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git switch dev
error: Your local changes to the following files would be overwritten by checkou
t:
        about.html
Please commit your changes or stash them before you switch branches.
Aborting

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git add .

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git commit -m "about changes"
[main 9dd0e06] about changes
 2 files changed, 13 insertions(+), 2 deletions(-)
 create mode 100644 team.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git switch dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (dev)
$ git add .

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (dev)
$ git commit -m "update"
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (dev)
$ git push
Everything up-to-date

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (dev)
$ git switch main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git push
To https://github.com/UmutesiMMA/Git-Redo.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/UmutesiMMA/Git-Redo.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git pull
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 2.35 KiB | 63.00 KiB/s, done.
From https://github.com/UmutesiMMA/Git-Redo
   81b8c35..9f059f0  main       -> origin/main
Merge made by the 'ort' strategy.
 README.md | 267 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 267 insertions(+)
 create mode 100644 README.md

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git push
Enumerating objects: 9, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 697 bytes | 232.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/UmutesiMMA/Git-Redo.git
   9f059f0..26c189e  main -> main

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ ls
README.md  about.html  home.html  index.html  start.html  style.css  team.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git branch ft/bundle-2

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git switch ft/bundle-2
Switched to branch 'ft/bundle-2'

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (ft/bundle-2)
$ touch services.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (ft/bundle-2)
$ git add .

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (ft/bundle-2)
$ git commit -m "services page"
[ft/bundle-2 72b6c7e] services page
 1 file changed, 17 insertions(+)
 create mode 100644 services.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (ft/bundle-2)
$ ^C

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (ft/bundle-2)
$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 484 bytes | 242.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/UmutesiMMA/Git-Redo/pull/new/ft/bundle-2
remote:
To https://github.com/UmutesiMMA/Git-Redo.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git pull
Already up to date.

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym2/Git (main)
$ git switch -c ft/service-redesign
Switched to a new branch 'ft/service-redesign'


```
