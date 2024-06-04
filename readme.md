# Git Bisect presentation

## What?

- pinpoint buggy commits using binary search

## Why?

- another tool in the toolbelt
- intempus is a prime example on how sometimes is a pain in the ass to find
the source of a bug introduced a few days ago, specially on how badly we use
git history
- not a tool for every bug

## Intro

- the usage is simple, you provide a GOOD commit, so a version of the code
that you KNOW that the bug wasn't introduced yet.
- then you provide a BAD commit, that you know the bug is present, git will
do the rest for you.
- sometimes you can even do automation on the whole process using scripts.

## Demo

```shell
git bisect start
git bisect bad HEAD (or the hash)
git bisect good (hash)

...
# auto run
git bisect start
git bisect bad HEAD (or the hash)
git bisect good (hash)
git bisect run ./test.sh
```
