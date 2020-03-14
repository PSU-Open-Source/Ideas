# A repo of ideas.

These are *some* (not all) of ideas I have had over the course of my time at
Portland State University in the post-bac and then the graduate program.

Some ideas may not be good (I did my best and left some out). Many of them don't have any implementation. 
But there is an idea behind them that, if pursued, could yield some useful tools (hopefully).

## Idea #1
**Summary**: Program that turns a drawing of a tree into a programmed AST.

**Prerequisites**: OCR and ability to fuse its results with programming languages concepts

**Details**: This program would be useful for those who don't want to code an AST or lack
the skills or knowledge. An AST has many [uses](https://en.wikipedia.org/wiki/Abstract_syntax_tree#Usage),
particulary, in compilers.
In addition, this program could implement methods. Ideally, the program would actaully 
have a set of pre-programmed methods and just replicate the data (i.e., the tree). 
This, in theory, would reduce the need for coders to code an AST.

## Idea #2
**Summary**: A program that memorizes (memoizes..?) previous input to a program. Monkey testing is
rarer these days, but not extinct.

**Prerequisites**: Probably *expect* or Pythons *pexpect* when replaying previous input and expecting previous output. 
Maybe the use of the unix program *tee* to keep track of input.

**Details**: This is a good tool for those that do user testing.

When a user tester is [monkey testing](https://www.softwaretestinghelp.com/what-is-monkey-testing-in-software-testing/)
a program they follow a linear path, starting at point 0 and moving to point x.

There are a few problems with this. 
1. When they have tested paths and received a segfault 
at path x, they have no way to return to the previous invocation/safe place before 
the segfault occurred and proceed 
to test further; they must start over at point 0. 
2. When a user is testing paths, 
they have no ability to determine if they have traversed all paths (and what values 
they have inputted) unless they manually write/type this.

A few possible solutions:
1. A program that memorizes (or memoizes) the input to a given program so it can be fed 
back in at a later date (e.g., by ./a.out > memorizedResults).
2. A GUI that draws a tree of possible paths and includes tested solutions the user has completed.
3. Additionally, a [symbolic execution engine](https://github.com/ksluckow/awesome-symbolic-execution#tools) could be run on the program pre-emptively and update 
the tree/picture to reduce user testing from needing to occur.
