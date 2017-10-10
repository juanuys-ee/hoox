# hoox
Useful Git hooks

**TL;DR** copy [prepare-commit-msg](prepare-commit-msg) and it will prepend the JIRA code from the branch name to your commit message if it doesn't have one already.

# commit-msg

    cp commit-msg .git/hooks/commit-msg

Checks whether your commit message contains a JIRA code.

# prepare-commit-msg

**Even better!**

    cp prepare-commit-msg .git/hooks/prepare-commit-msg


If your branch name and commit message BOTH contain a JIRA code, this script just warns you. Up to you, then, to rectify the situation with `git commit --amend`.

If NEITHER your branch name nor your commit message contains a JIRA code, it fails the same way as the `commit-msg` hook. 

If your branch name contains a JIRA code, but your commit message doesn't, it helpfully prepends the JIRA code to your commit message.

If your branch name does not contain a JIRA code, but the commit message does, do nothing.
