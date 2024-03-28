# Instalacje
https://git-scm.com/download/win

git --version
git version 2.43.0.windows.1


# Visual Studio
File -> Open -> Folder -> New Folder "altkom-git-marzec2" -> Select Folder

View -> Git Changes
Tools -> Options -> International Settings -> English

# Terminal
View => Terminal   Ctrl+`


# GIT Status
git status
fatal: not a git repository (or any of the parent directories): .git

# GIT Init
git init
Initialized empty Git repository in C:/Projects/altkom-git-marzec2/.git/

 git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .vs/
        Notatki.md

nothing added to commit but untracked files present (use "git add" to track)

git status
On branch master
nothing to commit, working tree clean

# Git config
C:\Users\<username>\.gitconfig


git config --local --list
.\.git\config


Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

# Git Commit
git status
git add plikA plikB zlyplik
git restore --staged zlyplik
git commit -m "Opis zmian"


# Vim
https://stackoverflow.com/questions/11828270/how-do-i-exit-vim
git commit
Esc :q! Enter  --- quit without saving
Aborting commit due to empty commit message.
Esc a      -- append mode
Esc :wq    -- write quit

git config --global core.editor="????"

git commit -am "Vim Editor"

# Git commit --amend
Git commit --amend  // VIM 
Git commit --amend  -m "💩"

## Poprawianie

git checkout fe124f345 -- tylko/ten/plik i/ten/plik

git checkout - zagl�da do wersji (przestawia tylko HEAD i czyta pliki) 

git checkout fe124f345  ## detached HEAD + git branch zapamietaj fe124f345

git checkout moj/branch123  ## przestawia HEAD i pliki
git switch  moj/branch123   ## przestawia HEAD i pliki


git reset -  ## przestawia etykiete(branch) ale zostawia pliki w changes 
git reset --hard  ## przestawia etykiete i HEAD - resetuje tez pliki

## Fast forward
Put this in $HOME/.gitconfig:

[merge]
    ff = no
#    commit = no

You can use git-config to do this:

#  git config --global merge.commit no
  git config --global merge.ff no


