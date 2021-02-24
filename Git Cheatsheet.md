# Git Cheatsheet

As you are working on a personal project as the sole contributor, your process will boil down to repeating 4 steps:

1. `git status`
2. `git add`
3. `git commit`
4. `git push`

## `git status`

Running `git status` will give you a rundown of all the new files that are untracked, have been modified or deleted since last commit.

Roughly equivalent to running `git status` is simply looking at the Source Control panel in VS Code.

## `git add`

Use `git add` to stage files for commit. To stage everything that is uncommitted, use `git add .`

You can also provide a space-delimited list of file paths to `git add`. For example, `git add index.html about/index.html neat.html`

You can also simply use the plus (+) icon in the Change subpanel of the Source Control panel of VS Code to stage files.

## `git commit`

Use `git commit` to commit your changes. You can use commit messages however you please, but my recommendations are as follows:

1. Commits should be frequent and small. Commits should represent distinct feature work. For example, if you work on `index.html` and `about.html` and the work you did in each is unrelated, I would stage each of those files separately and commit them separately, as they represent distinct "features".
2. Commit messages should be brief and descriptive. For example, avoid messages like "fixed bug" or "today's work". Instead, use "added new <li> tag for navigation" or "modified rules for .article class".
3. Avoid explaining your code in your commit messages. Let the code speak for itself. If its complicated and you want to leave yourself some notes, do so in a README.md file or leave comments in the code. 

The command to commit is `git commit -m <message>` where `-m` indicates that you are adding a commit message. For example, `git commit -m "modified rules for .article class"`

You can also use the Source Control panel in VS Code to type out your commit messages. Pressing `enter` gives you a new line in your commit message (there is something like a 70 character limit per line) and `ctrl + enter` will commit your changes.

**Remember** that you must stage a change before you can commit it.

## `git push`

The final step is to push your changes to the remote repo. The command is `git push origin main`, where `origin` is the name of your remote branch (google "git remotes" for more information) and `main` is the name of the branch that you want to push to.