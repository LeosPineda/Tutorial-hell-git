------GIT-----------

git --version

git config --global user.name "Leos C> Pineda III"
gt config --global user.email "oldleos1234@gmail.com"
git config --global core.editor "code --wait"

git config --list

Initialize repo

cd - changing th directory
pwd - display the current directory
git init - initialize repo
git status - shows the commited , staged, untracked and tracked files



ls- shows inside the workspace

git add <file> - Stage a file
git add --all or git add -A - Stage all changes
git status - See what is staged
git restore --staged <file> - Unstage a file
git add . stages all changes

git commit -m "message" - Commit staged changes with a message
git commit -a -m "message" - Commit all tracked changes (skip staging)
git log - See commit history


git branch "Testing" - to create a branch 
git branch - to check exisitng branch
git checkout "Testing2" - to change the main branch
git checkout -b feature/login ---- both the branch and checkout
git checkout  cb653133e9696d9e97b25f6914af5f506c55353a --- enter detached head state
git checkout -b <new-branch-name> <commit-hash> - to make a branch using the last commited files than can recover for main
git branch -d hello-world-images ----delete a branch

git stash - Stash your changes
git stash push -m "message" - Stash with a message
git stash list - List all stashes
git stash branch <branchname> - Create a branch from a stash

git merge - Merge a branch into your current branch
git merge --no-ff - Always create a merge commit
git merge --squash - Combine changes into a single commit
git merge --abort - Abort a merge in progress


git restore <file> - Undo changes in your working directory (before staging).
git restore --staged <file> - Unstage a file (move it out of the Staging Area).
git reset HEAD~ - Undo your last commit (keeps changes in your working directory).
git commit --amend - Change the last commit message or add files to your last commit.


------GITHUB--------
git push origin main ---- sends your commits to a remote repository like GitHub.
git pull origin main ---- brings commits from a remote repository down to your local copy.
git remote add origin https://github.com/your-username/your-repo.git
git branch -M main
git push -u origin main
git clone https://github.com/LeosPineda/E-COMMERCE_FIRST_PROJECT.git -----clone the repo in github
code e-commerce ---- open the clone

-----Troubleshooting----------
ls -a -----If .git appears there, you have a Git repo 
rm -rf .git -------- If you don’t want this folder to be a Git repo:
cd E-COMMERCE_FIRST_PROJECT -------- just cd into your actual cloned repo:
git status

---------Other Useful Commit Options---------
Create an empty commit:
git commit --allow-empty -m "Start project"
Use previous commit message (no editor):
git commit --no-edit
Quickly add staged changes to last commit, keep message:
git commit --amend --no-edit
Troubleshooting Common Commit Mistakes
Forgot to stage a file?
If you run git commit -m "message" but forgot to git add a file, just add it and commit again. Or use git commit --amend to add it to your last commit.
Typo in your commit message?
Use git commit --amend -m "Corrected message" to fix the last commit message.
Accidentally committed the wrong files?
You can use git reset --soft HEAD~1 to undo the last commit and keep your changes staged.

git tag <tagname> - Create a lightweight tag
git tag -a <tagname> -m "message" - Create an annotated tag
git tag <tagname> <commit-hash> - Tag a specific commit
git tag - List tags
git show <tagname> - Show tag details

git log - Show full commit history
git log --oneline - Show a summary of commits
git show <commit> - Show details of a specific commit
git diff - See unstaged changes
git diff --staged - See staged changes

git help <command> - See the manual page for a command
git <command> --help - See help for a command (same as above)
git <command> -h - See a quick summary of options
git help --all - List all possible Git commands
git help -g - List guides and concepts