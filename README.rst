Goal
====

Copy (e.g.) the Scala .gitignore template into my project in such a way that
the upstream version and my version can be kept in sync or diverge, and make it
so that it's very explicit what's happening.

Execution
=========
A subrepo_ is kept in a long running branch. (in this case ``gitignore``) I add
adapter commits on top of it to change the directory structure of the original
repo into what I want (e.g. 1e2c9417f25c0242eb723c0b39d6d46b1d3e5c0d) and I
merge that into the ``master`` branch. Then, to keep in sync, I go in the long
running branch, do a subrepo pull, and merge again.  Conflicts are often
brought up, but it's normally clear why they happened and trivial how to
respond to them.

.. _subrepo: https://github.com/ingydotnet/git-subrepo
