# Git hook sandbox
This project contains no real code aside from git hook experiments which are
meant to help support security checks in a CI/CD environment.
## Limitations
* Is it possible to enforce a `pre-commit` script as soon as a repository is
cloned or does it always need to be a manual step?
* Can we use symbolic links from `pre-commit.sh` to `.git/hooks/pre-commit`
or are hard links mandatory?
  * Symbolic links do not work, we *must* use hard links -- what does this
mean for filesystems which do no support hard links..?
