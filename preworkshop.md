Pre-workshop Instructions
=========================

We would like the workshop to be an interactive experience, were you get
to try everything yourself, rather than just watching someone else doing
it.  For this to happen, you will need to do some homework prior to the
workshop itself.

If you have trouble with the instructions below, there will be some
volunteers available before and during the workshop.  Plan on coming up
to half an hour early to get help with your issues.


1. Bring a laptop
-----------------

To take full advantage of the workshop, you will want to have a laptop
with you.  Many of the things we will be trying out are (much) harder to
get to work under Windows, so if you have the option, you want to bring
a Linux or OS X computer.


2. Install Git
--------------

You will need to have Git working on your system.  Unless you are using
Windows, you probably already have it on your system.  You can find
detailed instructions for any OS on
[Git's website](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).


3. Join GitHub
--------------

While there are other options out there, many FOSS projects in Python's
data science ecosystem are hosted on GitHub.  If you don't already, you
will want to have an account set up with them.  This is completely free,
but you will need to provide your e-mail address when signing up.
Follow the instructions on [GitHub's website](https://github.com/join).


4. Install Python
-----------------

You will need a Python distribution installed on your system.  Actually,
if you plan on doing any kind of serious development, you will likely
end up having a few of them.  There are several tools that help manage
this, each with its advantages and disadvantages.

For the purpose of this workshop, we will use Continuum's Anaconda
distribution, and their conda package manager.  To use this recommended
setup, start by installing Miniconda, following the instructions for
your OS on
[conda's documentation](http://conda.pydata.org/docs/install/quick.html).

After installing and updating conda itself per the above instructions,
create an environment for numpy development running from the command
line:

```
conda create -n numpydev35 python=3.5 nose cython
```

This will create an environment, called numpydev35, with the latest
Python version (3.5), and the dependencies required to build and test
the NumPy library.

If you are a Python 2.x kind of person, requesting `python=2.7` (and
changing the environment name accordingly) should do the trick for you.

After creating the environment, you can activate it by running from the
command line

```
source activate numpydev35
```

on Linus or OS X, or

```
activate numpydev35
```

under Windows.


5. Install a C compiler
-----------------------

Building NumPy requires a C compiler, so you want to make sure one is
properly installed.

 * If you are on a Linux system, chances are `gcc` is already installed,
   type `gcc --version` on the command line to confirm.
 * On OS X, you will need the xcode toolset.  On Yosemite, trying to run
   any development command, e.g. `gcc --version`, will display a pop-up
   window requesting permission to install it.  For earlier versions,
   manually [download](https://developer.apple.com/xcode/download/) and
   install it.
 * If you are a Windows user, you are about to enter a world of pain.
   Your best bet is installing [MinGW](http://www.mingw.org/), although
   this is far from a perfect solution.  If you go this route, do not
   install the latest Python version, settle with 3.4, as MinGW doesn't
   support it yet.
