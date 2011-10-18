git-subdirs
===========

*git-subdirs* is a small wrapper for performing Git commands on nested
repositories in subdirectories.


Usage
-----

Suppose we have the following directory structure inside the current directory:

    .
    +-- .git/
    +-- bin/
    +-- Desktop/
    +-- image/
    +-- src/
    |   |-- test1/
    |   |   `-- .git/
    |   |-- git-subdirs/
    |   |   `-- .git/
    |   |-- hgbook/
    ...

Let's invoke `git status` on all the Git repositories in the subdirectories:

    $ sgit status
    #
    # => Repository 'current'
    #
    # On branch master
    nothing to commit (working directory clean)
    #
    # => Repository 'src/test1'
    #
    # On branch master
    nothing to commit (working directory clean)
    #
    # => Repository 'src/git-subdirs'
    #
    # On branch master
    nothing to commit (working directory clean)


Requirements
------------

* `git`
* `python`
* `python-distribute`


Installation
------------

From the [Python Package Index][1] using `pip` or `easy_install`:

    $ pip install git-subdirs

Or manually from the GitHub:

    $ git clone git://github.com/vlasovskikh/git-subdirs.git
    $ cd git-subdirs
    $ python manage.py install --user


  [1]: http://pypi.python.org/

