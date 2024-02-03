## What is Git?
Git is *distributed version control software*. Version control is a way to save changes over time without overwriting previous versions. Being distributed means that every developer working with a Git repository has a copy of that entire repository - every commit, every branch, every file.

---

There are a few things you should know before getting started with Git:
- Branches are lightweight and cheap, so it's OK to have many of them.
- Git stores changes in SHA hashes, which work by compressing text files. That makes Git a very good version control system (VCS) for software programming, but not so good for binary files like images or videos.
- Git repositories can be connected, so you can work on one locally on your own machine, and connect it to a shared repository. This way, you can push and pull changes to a repository and easily collaborate with others.

## Why Use Git?
Version control is very important - without it, you risk losing your work. With Git, you can make a "commit", or a save point, as often as you'd like. You can also go back to previous commits. This takes the pressure off of you while you're working. Commit often and commit early, and you'll never have that gut sinking feeling of overwriting or losing changes.

There are many version control systems out there - but Git has some major advantages concerning speed, merge conflicts, cheap branches, and ease of roll back.

## Getting Started With Git
There are many ways to use Git, which doesn't necessarily make it easier! But, the fundamental Git workflow has a few main steps. You can practice all of these in the [Introduction to GitHub course](https://github.com/skills/introduction-to-github).

## [Visual Guide to Git Internals](https://www.freecodecamp.org/news/git-internals-objects-branches-create-repo/) — Objects, Branches, and How to Create a Repo From Scratch
Git Objects — blob, tree and commit

It is very useful to think about git as maintaining a file system, and specifically — snapshots of that system in time.

A file system begins with a root directory (in UNIX-based systems, /), which usually contains other directories (for example, /usr or /bin). These directories contain other directories, and/or files (for example, /usr/1.txt).

In git, the contents of files are stored in objects called blobs, binary large objects.

The difference between blobs and files is that files also contain meta-data. For example, a file “remembers” when it was created, so if you move that file into another directory, its creation time remains the same.

Blobs, on the other hand, are just contents — binary streams of data. A blob doesn’t register its creation date, its name, or anything but its contents.

Every blob in git is identified by its SHA-1 hash. SHA-1 hashes consist of 20 bytes, usually represented by 40 characters in hexadecimal form. Throughout this post we will sometimes show just the first characters of that hash.

In git, the equivalent of a directory is a tree. A tree is basically a directory listing, referring to blobs as well as other trees.

Trees are identified by their SHA-1 hashes as well. Referring to these objects, either blobs or other trees, happens via the SHA-1 hash of the objects.

...
