prasr@Prachi MINGW64 /c/gunjan/gunjan/git
$ git --version
git version 2.37.2.windows.2

prasr@Prachi MINGW64 /c/gunjan/gunjan/git
$ git status
fatal: not a git repository (or any of the parent directories): .git

prasr@Prachi MINGW64 /c/gunjan/gunjan/git
$ git init
Initialized empty Git repository in C:/gunjan/gunjan/git/.git/

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git add .

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   software.txt
        new file:   utility.txt


prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   software.txt
        new file:   utility.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   software.txt
        modified:   utility.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.txt


prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
        add

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git add .

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.txt
        new file:   software.txt
        new file:   utility.txt


prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git commit -m "version 10"
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'prasr@Prachi.(none)')

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git config --global user.name "gunjan"

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ ^C

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git config --global user.email "gunjanrawal7621@gmail.com"

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git commit -m "version 10"
[master (root-commit) 5435422] version 10
 3 files changed, 3 insertions(+)
 create mode 100644 README.txt
 create mode 100644 software.txt
 create mode 100644 utility.txt

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git log
commit 5435422c355bea50b0174aa963c99508c535ffe3 (HEAD -> master)
Author: gunjan <gunjanrawal7621@gmail.com>
Date:   Thu Feb 16 09:45:11 2023 +0530

    version 10

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git add .

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   software.html
        deleted:    software.txt


prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git commit -m
error: switch `m' requires a value

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git add --all

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   README.md
        deleted:    README.txt
        new file:   software.html
        deleted:    software.txt
        new file:   utility.css
        deleted:    utility.txt


prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git add -A

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git commit -m "first release to hello world"
[master f5bde17] first release to hello world
 6 files changed, 21 insertions(+), 3 deletions(-)
 create mode 100644 README.md
 delete mode 100644 README.txt
 create mode 100644 software.html
 delete mode 100644 software.txt
 create mode 100644 utility.css
 delete mode 100644 utility.txt

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   software.html

no changes added to commit (use "git add" and/or "git commit -a")

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git status --short
 M software.html

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   software.html

no changes added to commit (use "git add" and/or "git commit -a")

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git commit -a -m "updated html file"
[master 5e4030e] updated html file
 1 file changed, 1 insertion(+)

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git commit -help
usage: git commit [<options>] [--] <pathspec>...

    -q, --quiet           suppress summary after successful commit
    -v, --verbose         show diff in commit message template

Commit message options
    -F, --file <file>     read message from file
    --author <author>     override author for commit
    --date <date>         override date for commit
    -m, --message <message>
                          commit message
    -c, --reedit-message <commit>
                          reuse and edit message from specified commit
    -C, --reuse-message <commit>
                          reuse message from specified commit
    --fixup [(amend|reword):]commit
                          use autosquash formatted message to fixup or amend/reword specified commit
    --squash <commit>     use autosquash formatted message to squash specified commit
    --reset-author        the commit is authored by me now (used with -C/-c/--amend)
    --trailer <trailer>   add custom trailer(s)
    -s, --signoff         add a Signed-off-by trailer
    -t, --template <file>
                          use specified template file
    -e, --edit            force edit of commit
    --cleanup <mode>      how to strip spaces and #comments from message
    --status              include status in commit message template
    -S, --gpg-sign[=<key-id>]
                          GPG sign commit

Commit contents options
    -a, --all             commit all changed files
    -i, --include         add specified files to index for commit
    --interactive         interactively add files
    -p, --patch           interactively add changes
    -o, --only            commit only specified files
    -n, --no-verify       bypass pre-commit and commit-msg hooks
    --dry-run             show what would be committed
    --short               show status concisely
    --branch              show branch information
    --ahead-behind        compute full ahead/behind values
    --porcelain           machine-readable output
    --long                show status in long format (default)
    -z, --null            terminate entries with NUL
    --amend               amend previous commit
    --no-post-rewrite     bypass post-rewrite hook
    -u, --untracked-files[=<mode>]
                          show untracked files, optional modes: all, normal, no. (Default: all)
    --pathspec-from-file <file>
                          read pathspec from file
    --pathspec-file-nul   with --pathspec-from-file, pathspec elements are separated with NUL character


prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git help --all
See 'git help <command>' to read about a specific subcommand

Main Porcelain Commands
   add                  Add file contents to the index
   am                   Apply a series of patches from a mailbox
   archive              Create an archive of files from a named tree
   bisect               Use binary search to find the commit that introduced a bug
   branch               List, create, or delete branches
   bundle               Move objects and refs by archive
   checkout             Switch branches or restore working tree files
   cherry-pick          Apply the changes introduced by some existing commits
   citool               Graphical alternative to git-commit
   clean                Remove untracked files from the working tree
   clone                Clone a repository into a new directory
   commit               Record changes to the repository
   describe             Give an object a human readable name based on an available ref
   diff                 Show changes between commits, commit and working tree, etc
   fetch                Download objects and refs from another repository
   format-patch         Prepare patches for e-mail submission
   gc                   Cleanup unnecessary files and optimize the local repository
   gitk                 The Git repository browser
   grep                 Print lines matching a pattern
   gui                  A portable graphical interface to Git
   init                 Create an empty Git repository or reinitialize an existing one
   log                  Show commit logs
   maintenance          Run tasks to optimize Git repository data
   merge                Join two or more development histories together
   mv                   Move or rename a file, a directory, or a symlink
   notes                Add or inspect object notes
   pull                 Fetch from and integrate with another repository or a local branch
   push                 Update remote refs along with associated objects
   range-diff           Compare two commit ranges (e.g. two versions of a branch)
   rebase               Reapply commits on top of another base tip
   reset                Reset current HEAD to the specified state
   restore              Restore working tree files
   revert               Revert some existing commits
   rm                   Remove files from the working tree and from the index
   shortlog             Summarize 'git log' output
   show                 Show various types of objects
   sparse-checkout      Reduce your working tree to a subset of tracked files
   stash                Stash the changes in a dirty working directory away
   status               Show the working tree status
   submodule            Initialize, update or inspect submodules
   switch               Switch branches
   tag                  Create, list, delete or verify a tag object signed with GPG
   worktree             Manage multiple working trees

Ancillary Commands / Manipulators
...skipping...
   ls-remote            List references in a remote repository
   ls-tree              List the contents of a tree object
   merge-base           Find as good common ancestors as possible for a merge
   name-rev             Find symbolic names for given revs
   pack-redundant       Find redundant pack files
   rev-list             Lists commit objects in reverse chronological order
   rev-parse            Pick out and massage parameters
   show-index           Show packed archive index
   show-ref             List references in a local repository
   unpack-file          Creates a temporary file with a blob's contents
   var                  Show a Git logical variable
   verify-pack          Validate packed Git archive files

Low-level Commands / Syncing Repositories
   daemon               A really simple server for Git repositories
   fetch-pack           Receive missing objects from another repository
   http-backend         Server side implementation of Git over HTTP
   send-pack            Push objects over Git protocol to another repository
   update-server-info   Update auxiliary info file to help dumb servers

Low-level Commands / Internal Helpers
   check-attr           Display gitattributes information
   check-ignore         Debug gitignore / exclude files
   check-mailmap        Show canonical names and email addresses of contacts
   check-ref-format     Ensures that a reference name is well formed
   column               Display data in columns
   credential           Retrieve and store user credentials
   credential-cache     Helper to temporarily store passwords in memory
   credential-store     Helper to store credentials on disk
   fmt-merge-msg        Produce a merge commit message
   hook                 Run git hooks
   interpret-trailers   Add or parse structured information in commit messages
   mailinfo             Extracts patch and authorship from a single e-mail message
   mailsplit            Simple UNIX mbox splitter program
   merge-one-file       The standard helper program to use with git-merge-index
   patch-id             Compute unique ID for a patch
   sh-i18n              Git's i18n setup code for shell scripts
   sh-setup             Common Git shell script setup code
   stripspace           Remove unnecessary whitespace

External commands
   askpass
   askyesno
   credential-helper-selector
   credential-manager-core
   flow
   lfs
   update-git-for-windows

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git branch hello-world-images

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git branch
  hello-world-images
* master

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git checkout hello-world-images
Switched to branch 'hello-world-images'

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (hello-world-images)
$ git branch
* hello-world-images
  master

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (hello-world-images)
$ git add --all

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (hello-world-images)
$ git status
On branch hello-world-images
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   images (2).jpg
        modified:   software.html


prasr@Prachi MINGW64 /c/gunjan/gunjan/git (hello-world-images)
$ git commit -m "image is added to our project"
[hello-world-images 6168d66] image is added to our project
 2 files changed, 2 insertions(+)
 create mode 100644 images (2).jpg

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (hello-world-images)
$ ls
 README.md  'images (2).jpg'   software.html   utility.css

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (hello-world-images)
$ git checkout master
Switched to branch 'master'

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ ls
README.md  software.html  utility.css

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git checkout -b emergency flix
fatal: 'flix' is not a commit and a branch 'emergency' cannot be created from it

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git checkout -b emergency-flix
Switched to a new branch 'emergency-flix'

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (emergency-flix)
$ git branch
* emergency-flix
  hello-world-images
  master

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (emergency-flix)
$ ls
README.md  software.html  utility.css

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (emergency-flix)
$ git add .

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (emergency-flix)
$ git commit -m "emergency_flix commit"
[emergency-flix e576a5c] emergency_flix commit
 1 file changed, 1 insertion(+), 1 deletion(-)

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (emergency-flix)
$ git checkout master
Switched to branch 'master'

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git merge emergency-flix
Updating 5e4030e..e576a5c
Fast-forward
 utility.css | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$ git branch -d emergency-flix
Deleted branch emergency-flix (was e576a5c).

prasr@Prachi MINGW64 /c/gunjan/gunjan/git (master)
$
