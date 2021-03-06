## my cheatsheet git commands

- configure default editor for commit messages
```git config --global core.editor "code --wait"```

- get the status on the recent dir 
``` git status ```

- get all commits existing in the current dir
``` git log ``` or to format ```git log --oneline```

- stage a file in a the current dir
``` git add <file_name> ```

- stage all files in the current  dir
``` git add .```

- amend the previous commit message
```git commit --amend ``` 
- shortcut for staging and committing
``` git commit -a -m"message" ```
- list all branches existing in the current directory (CD)
``` git branch ```

- create a new branch
``` git branch <branch-name>```
    > will not swith to the created branch.

- once you have created a new branch, we can switch to it
``` git switch <branch-name>``` or  ``` git checkout <branch-name>```
    > to create a branch and switch on it ``` git switch -c <branch-name>``` or  ``` git checkout -b <branch-name>```

- delete a branch
``` git branch -D <branch-name>```
    > we have to be into another branch while trying to delete a branch
 - rename a branch
 ``` git branch -m <branch-name>```
    > we should be within the branch we want to rename

- commit the new created  local branch with his content 
    ```git push --set-upstream origin <branch_name>```

- combine two branch, move to the destination branch and then use the following cmd
``` git merge <branch-name>```
    > A fast-forward merge can occur when there is a linear path from the current branch tip to the target branch.
    > In the event that you require a merge commit during a fast forward merge for record keeping purposes you can execute git merge with the --no-ffoption. ```git merge --no-ff <branch-name>```

- view changes between commits, branches, files , our working dir ...etc itshow the difference between new changes and the last commit 
    ``` git diff ``

    > `git diff --staged` or `--cached` will list the changes between the staging area and our last commit, and to view for a particular field we can add the specific <file_name> in option as `git diff HEAD [file_name]` or compre twoo files `git diff [file_name_1] [file_name_2]`