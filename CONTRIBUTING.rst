============
Contributing
============

Contributions are welcome, and they are greatly appreciated! Every
little bit helps, and credit will always be given. 

You can contribute in many ways:

Types of Contributions
----------------------

Report Bugs
~~~~~~~~~~~

Report bugs at https://github.com/mihassan/python_algorithms/issues.

If you are reporting a bug, please include:

* Your operating system name and version.
* Any details about your local setup that might be helpful in troubleshooting.
* Detailed steps to reproduce the bug.

Fix Bugs
~~~~~~~~

Look through the GitHub issues for bugs. Anything tagged with "bug"
is open to whoever wants to implement it.

Implement Features
~~~~~~~~~~~~~~~~~~

Look through the GitHub issues for features. Anything tagged with "feature"
is open to whoever wants to implement it.

Write Documentation
~~~~~~~~~~~~~~~~~~~

Python Algorithms could always use more documentation, whether as part of the 
official Python Algorithms docs, in docstrings, or even on the web in blog posts,
articles, and such.

Submit Feedback
~~~~~~~~~~~~~~~

The best way to send feedback is to file an issue at https://github.com/mihassan/python_algorithms/issues.

If you are proposing a feature:

* Explain in detail how it would work.
* Keep the scope as narrow as possible, to make it easier to implement.
* Remember that this is a volunteer-driven project, and that contributions
  are welcome :)

Get Started!
------------

Ready to contribute? Here's how to set up `python_algorithms` for local development.

1. Fork the `python_algorithms` repo on GitHub.

2. Clone your fork locally::

    $ git clone git@github.com:your_name_here/python_algorithms.git

3. Install your local copy into a virtualenv. Assuming you have virtualenvwrapper installed, this is how you set up your fork for local development::

    $ mkvirtualenv pyalgs
    $ cd pyalgs/
    $ python setup.py develop

4. Create a branch for local development::

    $ git checkout -b name-of-your-bugfix-or-feature
   
   Now you can make your changes locally.

   Alternatively, use git flow to start a new feature or bugfix branch and work
   on that branch locally. Once, ready to publish, push the branch to github::

    $ git flow feature start name-of-feature
    $ echo "Develop the feature on this feature branch"
    $ git flow feature finish
    $ git push

5. When you're done making changes, check that your changes pass flake8 and the tests, including testing other Python versions with tox::

    $ flake8 pyalgs tests
    $ python setup.py test
    $ tox

   To get flake8 and tox, just pip install them into your virtualenv. 

6. Commit your changes and push your branch to GitHub::

    $ git add .
    $ git commit -m "Your detailed description of your changes."
    $ git push origin name-of-your-bugfix-or-feature

7. Submit a pull request through the GitHub website.

Update Python Packages
----------------------

Be mindful of updating packages as it may break some dependencies. Still, from time to time we need to update the packages following these steps::

    1. $ pip freeze --local | grep -v '^\-e' | cut -d = -f 1  | xargs -n1 pip install -U
    
    2. $ pip freeze --local -r requirements.txt > requirements.txt 


Pull Request Guidelines
-----------------------

Before you submit a pull request, check that it meets these guidelines:

1. The pull request should include tests.
2. If the pull request adds functionality, the docs should be updated. Put
   your new functionality into a function with a docstring, and add the
   feature to the list in README.rst.
3. The pull request should work for Python 2.6, 2.7, 3.3, 3.4, and 3.5, and for PyPy.
   Check https://travis-ci.org/mihassan/python_algorithms/pull_requests
   and make sure that the tests pass for all supported Python versions.

Tips
----

To run a subset of tests::

	$ python -m unittest tests.test_pyalgs