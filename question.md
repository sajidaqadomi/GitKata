## What's the content of file.txt?
>> It is empty 

▶️ **Overwrite the content in file.txt:**
echo 2 > file.txt will change the content of file.txt to "2."

## What does git diff tell you?
>> it is blank as git diff shows the difference between the changes made to the working directory and the last commit.

## What does git diff --staged tell you?
>> it is blank as git diff --staged (or git diff --cached) shows the difference between the changes that have been staged and the last commit. 

▶️ **Run git add file.txt to stage your changes from the working directory.**

## What does git diff tell you?
it is not showing any differences because the changes are now staged.

## What does git diff --staged tell you?

```
$ git diff --staged
diff --git a/file.txt b/file.txt
new file mode 100644
index 0000000..0cfbf08
--- /dev/null
+++ b/file.txt

```

▶️ **Overwrite the content in file.txt:**
Running the command echo 3 > file.txt

## What does git diff tell you?
it show the changes made to file.txt (from "2" to "3").

```
diff --git a/sa.txt b/sa.txt
index 0cfbf08..00750ed 100644
--- a/sa.txt
+++ b/sa.txt
@@ -1 +1 @@
-2
+3 
```

## What does git diff --staged tell you?

```
$ git diff --staged
diff --git a/sa.txt b/sa.txt
new file mode 100644
index 0000000..0cfbf08
--- /dev/null
+++ b/sa.txt
@@ -0,0 +1 @@
+2 ✅
```

## Explain what is happening:
git diff --staged ➡️ shows only the modifications that have been made to the staged or tracked files
git diff ➡️ show all changes to tracked files. If you have all changes staged for commit, then both commands will output the same.

▶️ **Run git status and observe that file.txt is present twice in the output**

```
No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   sa.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   sa.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        file.txt
        question.md

```

▶️ **Run git restore --staged file.txt to unstage the change**

## What does git status tell you now?
```
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        file.txt
        question.md
        sa.txt

nothing added to commit but untracked files present (use "git add" to track)

```

## Stage the change and make a commit:
 ```
git commit -a -m "Commit message"
 ```

## What does the log look like?
The commit log show the history of commits.

## Overwrite the content in file.txt:
echo 4 > file.txt 

## What is the content of file.txt?
the content of file.txt is "4."

## What does git status tell us?
sa.txt has been modified but not yet staged.

```
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   sa.txt

```

▶️ **Run git restore file.txt**

## What is the content of file.txt?
the content of file.txt will be the same as it was in the last commit.


## What does git status tell us?

```
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   sa.txt

```
