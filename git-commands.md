# Git

## Initialising a git repository

Either we can clone an existing git repository
Or we can turn our project in local machine to git repository

### 1. Cloning an Existing Repository

Use: `git clone <url>`

### 2. Initializing a Repository in an Existing Directory & Adding files

- `git init` to initialise a repository.

- `git add <filename>` to specify the files you have to track using Git. Now its under staged because it’s under the “Changes to be committed”.
  git add is a multipurpose command, you use it to begin tracking new files, to stage files, and to do other things like marking merge-conflicted files as resolved.

- `git commit -m "commit-msg"` to commit the files from the staging area.
  - `git commit -a -m "commit-msg"` in this `-a` will help to skip the staging area and directly commit the modified files.

## Git Commands

- `git status` to get the status
- `git status -s` or `git status --short` will give more simplified output.
  eg:

  ```
  $ git status -s
  M README
  MM Rakefile
  A  lib/git.rb
  M  lib/simplegit.rb
  ?? LICENSE.txt
  ```

  - ??: new files that aren’t tracked
  - A: new files that have been added to the staging area
  - M: modified files
  - left-hand column: the status of the staging area
  - right-hand column: the status of the working tree.
  - eg: Rakefile was modified, staged and then modified again, so there are changes to it that are both staged and unstaged.

- `.gitignore ` : files or folders to be ignored by git.

- `git diff` : shows what exactly is changed, to be stages, to be committed etc. rather than file names.
