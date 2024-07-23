# gitAdventure
gitAdventure


15035@HyunAsus MINGW64 ~
$ git --version
git version 2.45.2.windows.1

15035@HyunAsus MINGW64 ~
$ https://git-scm.com/downloads
bash: https://git-scm.com/downloads: No such file or directory

15035@HyunAsus MINGW64 ~
$ git config --global user.name "Ryan Kim"

15035@HyunAsus MINGW64 ~
$ git config --global user.email rlagusxo52@gmail.com

15035@HyunAsus MINGW64 ~
$ mkdir GitAdventure

15035@HyunAsus MINGW64 ~
$ cd GitAdventure

15035@HyunAsus MINGW64 ~/GitAdventure
$ git init
Initialized empty Git repository in C:/Users/15035/GitAdventure/.git/

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ echo "Embarking on my journey to master Git." > journey.txt

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        journey.txt

nothing added to commit but untracked files present (use "git add" to track)

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git config --global user.name "Ryan Kim"

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git config --global user.name "rlagusxo52@gmail.com"

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        journey.txt

nothing added to commit but untracked files present (use "git add" to track)

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git add journey.txt
warning: in the working copy of 'journey.txt', LF will be replaced by CRLF the next time Git touches it

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ echo "This file is meant to be deleted." > temp.txt

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ add temp.txt
bash: add: command not found

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ commit -m "Prepare temp.txt for deletion"
bash: commit: command not found

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git add temp.txt
warning: in the working copy of 'temp.txt', LF will be replaced by CRLF the next time Git touches it

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git commit -m "Prepare temp.txt for deletion"
[master (root-commit) 5d98ee1] Prepare temp.txt for deletion
 2 files changed, 2 insertions(+)
 create mode 100644 journey.txt
 create mode 100644 temp.txt

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git rm temp.txt
rm 'temp.txt'

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git commit -m "Delete temp.txt"
[master 599130e] Delete temp.txt
 1 file changed, 1 deletion(-)
 delete mode 100644 temp.txt

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git mv journey.txt adventure.txt

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ echo "My journet evolves into an adventure with Git." >adventure.txt

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git add adventure.txt
warning: in the working copy of 'adventure.txt', LF will be replaced by CRLF the next time Git touches it

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git commit -m "Rename journey.txt to adventure.txt and update content"
[master 788ed23] Rename journey.txt to adventure.txt and update content
 2 files changed, 1 insertion(+), 1 deletion(-)
 create mode 100644 adventure.txt
 delete mode 100644 journey.txt

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ echo "*.log" > .gitignore

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git add .gitignore
warning: in the working copy of '.gitignore', LF will be replaced by CRLF the next time Git touches it

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git commit -m "Add .gitignore to ignore log files"
[master f18c4e2] Add .gitignore to ignore log files
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ touch test.log

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git status
On branch master
nothing to commit, working tree clean

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ echo "Exploring the depths of git commands and their powers." >>adventure.txt

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git status -s
 M adventure.txt

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git add adventure.txt
warning: in the working copy of 'adventure.txt', LF will be replaced by CRLF the next time Git touches it

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git commit -m "Update adventure.txt with exploration insights"
[master f3c0dd0] Update adventure.txt with exploration insights
 1 file changed, 1 insertion(+)

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git log --oneline --reverse
5d98ee1 Prepare temp.txt for deletion
599130e Delete temp.txt
788ed23 Rename journey.txt to adventure.txt and update content
f18c4e2 Add .gitignore to ignore log files
f3c0dd0 (HEAD -> master) Update adventure.txt with exploration insights

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git restore --source=<commit_id> adventure.txt
bash: commit_id: No such file or directory

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git add adventure.txt

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git commit -m "Revert adventure.txt to its initial state"
On branch master
nothing to commit, working tree clean

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ ls-tree
bash: ls-tree: command not found

15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git ls-tree
usage: git ls-tree [<options>] <tree-ish> [<path>...]

    -d                    only show trees
    -r                    recurse into subtrees
    -t                    show trees when recursing
    -z                    terminate entries with NUL byte
    -l, --long            include object size
    --name-only           list only filenames
    --name-status         list only filenames
    --object-only         list only objects
    --[no-]full-name      use full path names
    --[no-]full-tree      list entire tree; not just current directory (implies --full-name)
    --format <format>     format to use for the output
    --[no-]abbrev[=<n>]   use <n> digits to display object names


15035@HyunAsus MINGW64 ~/GitAdventure (master)
$ git ls-files
.gitignore
adventure.txt
