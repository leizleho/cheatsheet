# Git Cheat Sheet
<hr>
![Git](img/gitlogo.png)
<hr>

## Git Configuration

##### Setup Git configuration
```
$ git config --global user.email "you@yourdomain.com"

$ git config --global user.name "FirtName LastName"

$ git config --global core.editor vi

$ git config --global color.ui true
```

##### Show current configuration
```
$ git config --list
```
##### Show repository configuration
```
$ git config --local --list
```
##### Show global configuration
```
$ git config --global --list
```
##### Show system configuraion
```
$ git config --system --list
```
<br>

## Create Repository

##### Initialize a local repository
```
$ git init
```
##### Clone an existing repository via HTTP
```
$ git clone htttp://domain.com/user/repo.git
```
##### Clone an existing repository via SSH
```
$ git clone ssh://user@domain.com/repo.git
```
<br>

## Local Changes

##### Add a file to the repo
```
$ git add <filename>
```

##### Add all the files to the repo 
```
$ git add .
```

##### Commit the change to git
```
$ git commit -m "Message about the change goes here" <filename>
```

##### Commit all changes to git of muliple files - no filenames needed
```
$ git commit -am "Message about the change goes here"
```

##### Check files are not added or committed from Working to Staging to Repository
```
$ git status
```
##### Commit changes to all files that are in Staging into Repo
```
$ git commit -m ""
```
##### Show changes between Working and Local Repo, no file supplied shows all files 
```
$ git diff
```
##### Show changes between Staged and Local Repo
```
$ git diff --staged
```
##### Remove file from working then git commit -m "" to also remove from Repo
```
$ git rm file.txt
```
##### leaves copy of file in Working but removes from Staging and Repo
```
$ git rm --cached file.txt
```

##### Rename or move files - then git commit -m "" to move to Repo
```
$ git mv
```
##### Restore Repo file to Working Directory using current branch
```
$ git checkout -- file.txt
```

## Commit History

##### Show the commit history
```
$ git log
```
##### Show all commits of a specific user
```
$ git log --author="username"
```
##### Show changes over time for a specific file
```
$ git log -p <file>
```
##### Show who changed what and when in a file
```
$ git blame <file>
```

## Publish
##### Show all current configured remotes
```
$ git remote -v
```
##### Show all remote
```
$ git remote 
```
##### Show remote URL
```
$ git remote show origin
```
##### Remove remote
```
$ git remote remove origin

$ git remote rm origin
```
##### Push from local to remote [push to remote(origin) and branch(master)]
```
$ git push -u origin master
```

