# 191-YingshanGuan

---------

## Basic Commits
1. git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

2. git log 
fatal: your current branch 'master' does not have any commits yet

3. touch testfile

4. git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        testfile

nothing added to commit but untracked files present (use "git add" to track)

5. git add testfile

6. git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   testfile

7. git commit
[master (root-commit) 78fbfaf] first file commit
 1 file changed, 0 insertions(+), 0 deletions(-)

8. git status
On branch master
nothing to commit, working tree clean

9. vim testfile and write to the file "something"

10. git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   testfile

no changes added to commit (use "git add" and/or "git commit -a")

11. git add testfile
warning: LF will be replaced by CRLF in testfile.
The file will have its original line endings in your working directory

12. git status 
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   testfile

13. vim testfile and write another line to it

14. git commit
[master 5884b37] second commit
 1 file changed, 1 insertion(+)

15. git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   testfile

no changes added to commit (use "git add" and/or "git commit -a")

------------

git log
commit 5884b376ba4dc50a01931d80cc6fc356b4b6d771 (HEAD -> master)
Author: yingshanguan <yingshag@uci.edu>
Date:   Fri Jan 24 20:50:36 2020 -0800

    second commit

commit 78fbfaf7b0065694418b7625fa4240e1bb579597
Author: yingshanguan <yingshag@uci.edu>
Date:   Fri Jan 24 20:45:37 2020 -0800

    first file commit
 
 
I realize that I didn't git add the changed file first before commit

16. after commiting the newest change
git status
On branch master
nothing to commit, working tree clean

-------------

##3 way merge
8. 
git log --oneline --graph --all
* 1e480fa (HEAD -> master) add README file
| * fb51629 (greeting) change in greeting file
|/
* 09a6ccf Add content to greeting.txt
* 13b0c29 Add file greeting.txt

10.
git merge master greeting
Merge made by the 'recursive' strategy.
 greeting.txt | 1 +
 1 file changed, 1 insertion(+)





