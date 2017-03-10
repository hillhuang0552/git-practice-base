# git-practice-base

A git repositorey to practice some git controls.


## Before Start

Fork this repo to your account.


## Basic

Clone this repo:

    git clone https://github.com/othree/git-practice-base.git

Replace `othree` with your account id.

Edit `README.md`. Then commit.

### Edit commit message

    git commit --amend

or by `reset`

    git reset --soft HEAD^

zsh:

    git reset --soft HEAD\^

Git reset can used to edit entire commit.


## Merge

Fecth and track all branches: <https://gist.github.com/othree/d9cefd1c4b5bb667d2690330231d5fff>

Or `checkout` before merge/rebase...

	git co for-fast-forward

Checkout `master`

    git co master

Fast forward merge:

    git merge for-fast-forward

None fast forward merge:

    git merge for-no-fast-forward --no-ff


## Rebase

Checkout `master`

    git co master

Rebase without any conflict:

    git rebase for-rebase

Rebase and will have conflict:

    git rebase for-rebase-conflict

Solve conflicts then:

	git add src/es2015-script.js
	git rebase --continue

Try `rebase continue --skip`:

    git rebase for-rebase-conflict-skip

Saw conflicts, and skip changes(Use HEAD reversion, a.k.a master):

    git rebase --skip
