# About Git `push`, `pull`, and `fetch` commands #

When you work with Git, it is essential to understand the differences between `push`, `pull`, and `fetch`. These commands are often confused because they perform some of the same functions, using different methods.

- `push` - Sends changes you make on your local branch to a remote repository.
When you `push`:
	1. Git verifies whether your tracking branch exists.
	2. Git verifies if a remote repository is connected to your tracking branch. Git does not perform a `fetch` when you `push`.
	3. If verification succeeds, Git sends the changes in your tracking branch to the remote branch. 

    To avoid merge conflicts, run `fetch` before running `push`. Running `fetch` before `push` synchronizes your tracking branch with the remote repository. If pushing fails, use `pull` to update and synchronize your tracking branch with the remote repository.
- `pull` - Updates your tracking branch with changes from a remote branch and merges the changes into your local branch. When you `pull`:
 
	1. Git perform a `fetch` command, which updates your tracking branch with changes from a remote repository.
	2. Git runs a `merge` command, which merges the changes from the remote repository with the changes in your tracking branch.
- `fetch` - Retrieves changes from a remote repository to your tracking branch. When you `fetch`:
	1. Git verifies whether your tracking branch exists.
	2. If verification succeeds, Git looks for changes in the remote branch that do not exist in your tracking branch.
	3. If there are changes, Git retrieves the changes but does not update the tracking branch.

    After you `fetch`, verify the changes Git has made to your tracking branch. Run `git merge origin/master` to synchronize your tracking branch and the remote repository.

