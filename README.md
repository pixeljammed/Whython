# Whython
Python with a dash of Lua. Because Lua is awesome - but nobody ever uses it for anything - lol!

Whython is a Python preprosessor which does stupid things, like force you to put **end** at the end of an indentation.

Forked from Bython.


## Content of README:
  * [Key features](#key-features)
  * [Code example](#code-example)
  * [Installation](#installation)
  * [Quick intro](#quick-intro)
  * [Structure of the repository](#structure-of-the-repository)


## Key features

 * Ponder why I even made this for anything other than a crap hobby project I won't update for yonkertons.

 * Uses Python for interpretation, that means that all of your existing modules, like NumPy and Matplotlib still works.


## Code example

```python
def scream(shout, count)
    for x in range(count) do
        print(shout);
    end
end

if __name__ == "__main__" then
    print_message(10);
end
```


## Installation

You can install Bython directly from PyPI using pip (with or without `sudo -H`, depending on your Python installation):

```
$ sudo -H pip3 install bython
```

If you for some reason want to install it from the git repository you can use `git clone` and do a local install instead:

```
$ git clone https://github.com/mathialo/bython.git
$ cd bython
$ sudo -H pip3 install .
```

The git version is sometimes a tiny bit ahead of the PyPI version, but not significantly.

To uninstall, simply run 

```
$ sudo pip3 uninstall bython
```

which will undo all the changes.



## Quick intro

Bython works by first translating Bython-files (suggested file ending: .by) into Python-files, and then using Python to run them. You therefore need a working installation of Python for Bython to work.


To run a Bython program, simply type

```
$ bython source.by arg1 arg2 ...
```

to run `source.by` with arg1, arg2, ... as command line arguments. If you want more details on how to run Bython files (flags, etc), type

```
$ bython -h
```

to print the built-in help page. You can also consult the man page by typing

```
$ man bython
```

Bython also includes a translator from Python to Bython. This is found via the `py2by` command:

```
$ py2by test.py
```

This will create a Bython file called `test.by`. A full explanation of `py2by`, is found by typing

```
$ py2by -h
```

or by consulting the man page:

```
$ man py2by
```

For a more in-depth intro, consult the [bython introduction](INTRODUCTION.md)


## Structure of the repository

At the moment, Bython is written in Python. The git repository is structured into 4 directories:

 * `bython` contains a Python package containing the parser and other utilities used by the main script
 * `etc` contains manual pages and other auxillary files
 * `scripts` contains the runnable Python scripts, ie the ones run from the shell
 * `testcases` contains a couple of sample \*.by and \*.py files intended for testing the implementation

