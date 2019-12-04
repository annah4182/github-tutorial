# GitHub Tutorial

_by Anna Huang_

---
## Git vs. GitHub
##### _What is the difference between them?_

Git is like a version control system storing all the repositories.
* runs in the command line
* used in the local remote
* useful for version control
GitHub on the other hand, 
* stores the code into the cloud
* visually tracks changes 
* collaboration on any files is allowed

---
## Initial Setup
To create a GitHub account:
1. [Go to GitHub](www.github.com)
2. Click sign up
3. Insert your email, username, and password

_* If you are a student at HSTAT, use your HSTAT email, but without the @hstat.org when inserting your username_

Setting up your IDE:
* Directions are here in this [link](https://github.com/hstatsep/ide50)

**What is the SSH key?** SSH key, known as the Secure Shell is a one time setup where it doesn't require you to enter your username and password everytime.
**Why do we need SSH?** We need the SSH keys to make sure that the user is interacting with the repository.



---
## Repository Setup
1. Have a directory that's different from the root directory using mkdir
2. Once created, you cd into it
3. When you're inside the folder, use git init to make it turn to a repo. To check that you have done it right, you should see the word "master"
4. Create a file using touch <file name> and c9 <file name> in order to go into the file  to edit and make changes
5. When you're done with your editings, use git add to include the changes onto the staging area
6. Lastly, use git commit -m "message" to label the specific changes you made
_**Use git add and git commit when you making new changes in the file**_

To link repository into IDE:
1. Always make sure that you are logged into Github
2. Click on the plus sign that's located on the upper right corner
3. Select "New repository"
4. Type in the same name/title that;s in your ide
5. Click on the "Create repository" button
6. There's two choices given, SSH and HTTPS. Make sure to use the SSH one
7. As you choose the SSH option, there will be something that looks like this:
git remote add origin git@github.com:<your github account>/<name of your repository>.git
git push -u origin master
8. Copy and paste it into your repo




---
## Workflow & Commands
* **git status** - an optional command that lets the programmer locate which files are staged for the commit (stated in green and in red if it's not committed)
* **git add** - used when you are adding all files that have been edited (also includes the ones that are deleted or renamed) onto the staging area
* ** git commit -m "message"** - takes a snapshot of the files on the stage
  _NOTE: the message should be in present-tense and describe what was changed in the snapshot_
* **git push** - sends any changes from the local repo "up" (cloud, aka ide) to the remote repo (GitHub)


---
## Rolling Back Changes
To undo an edit, git checkout --  filename should be used. This undos the recent changes you have done.

To undo an add, use git reset HEAD filename. THis removes the revisions from the stage area

To undo a commit, use git reset --soft HEAD~1, to save the undone changes OR git reset --hard HEAD~1 to fully delete the edits/changes

To undo a push, type git log and look for SHA, the commit that you choose to revert back. Type git revert and copy/paste the SHA. Then, use git reset HEAD^ --hard and git push origin master for the commites to be the same in the cloud and the remote