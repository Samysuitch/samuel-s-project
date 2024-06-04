# Git exercise solutions
my project on github
## Boundle 1
### Exercise 1
``` bash
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git init
Initialized empty Git repository in C:/Users/IYAKAREMYE Samuel/OneDrive/Desktop/samuel's project/git solutions/.git/
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git branch -M master main
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git add --all
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git commit -m " my project 1"
[main (root-commit) a113937]  my project 1
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Readme.md
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git remote add origin https://github.com/Samysuitch/samuel-s-project.git
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 222 bytes | 111.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Samysuitch/samuel-s-project.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git checkout dev
Switched to branch 'dev'
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git checkout -d test
HEAD is now at a113937  my project 1
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions>
```
### Exercise 2
``` bash
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git add home1.html
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git stash
Saved working directory and index state WIP on dev: b6a9f12 my project
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git stash list
stash@{0}: WIP on dev: b6a9f12 my project
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git add about.html
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git stash
Saved working directory and index state WIP on dev: b6a9f12 my project
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git add team.html
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git stash
Saved working directory and index state WIP on dev: b6a9f12 my project
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git stash list
stash@{0}: WIP on dev: b6a9f12 my project
stash@{1}: WIP on dev: b6a9f12 my project
stash@{2}: WIP on dev: b6a9f12 my project
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git stash pop stash@"{1}"
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (d65ce5d3aead66d9564dd5cf71b9e4f77e08a16e)
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git stash list
stash@{0}: WIP on dev: b6a9f12 my project
stash@{1}: WIP on dev: b6a9f12 my project
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git stash pop stash@"{1}"
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home1.html

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    homee.html

Dropped stash@{1} (37878947ddc1caa622bb19ba3222926f134a255a)
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home1.html

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    homee.html

PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git add about.html home1.html
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git commit -m "my project"
[dev fa433b5] my project
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 about.html
 create mode 100644 home1.html
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git push --set-upstream origin dev
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 866 bytes | 433.00 KiB/s, done.
Total 7 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Samysuitch/samuel-s-project/pull/new/dev
remote:
To https://github.com/Samysuitch/samuel-s-project.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git stash list
stash@{0}: WIP on dev: b6a9f12 my project
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git stash pop stash@"{0}"
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    homee.html

Dropped stash@{0} (8302cab009e8689deb8efb9a23248eb7eb29a6bd)
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git reset --hard
HEAD is now at fa433b5 my project
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions>
```
## boundle 2
### exercise 1
``` bash
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git add service.html
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git commit -m "our service"
[ft/bundle-2 059bbc0] our service
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 service.html
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git push --set-upstream origin ft/bundle-2
fatal: unable to access 'https://github.com/Samysuitch/samuel-s-project.git/': Could not resolve host: github.com
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> git push --set-upstream origin ft/bundle-2
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 250 bytes | 250.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Samysuitch/samuel-s-project/pull/new/ft/bundle-2
remote:
To https://github.com/Samysuitch/samuel-s-project.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
PS C:\Users\IYAKAREMYE Samuel\OneDrive\Desktop\samuel's project\git solutions> 
```
### exercise 2
