==========
Installing
==========

Prerequisites
-------------

* Python interpreter
* Adjust your path
* Packaging tools

Python Interpreter
^^^^^^^^^^^^^^^^^^

Install Python for your operating system. Consult the official `Python
documentation <https://docs.python.org/3/using/index.html>`_ for details.

You can install the Python binaries from `python.org
<https://www.python.org/downloads/mac-osx/>`_. Alternatively on macOS, you can
use the `homebrew <http://brew.sh/>`_ package manager.

.. code-block:: bash

    # for python 3.x
    $ brew install python3

Adjust your path
^^^^^^^^^^^^^^^^

Ensure that your ``bin`` folder is on your path for your platform. Typically
``~/.local/`` for UNIX and macOS, or ``%APPDATA%\Python`` on Windows. (See the
Python documentation for `site.USER_BASE
<https://docs.python.org/3/library/site.html#site.USER_BASE>`_ for full
details.)


UNIX and macOS
""""""""""""""

For bash shells, add the following to your ``.bash_profile`` (adjust for other
shells):

.. code-block:: bash

    # Add ~/.local/ to PATH
    export PATH=$HOME/.local/bin:$PATH

Remember to load changes with ``source ~/.bash_profile`` or open a new shell
session.


Windows
"""""""

Ensure the directory where DocSwitch will be installed is in your
environment's ``Path`` in order to make it possible to invoke it from a command
prompt. To do so, search for "Environment Variables" on your computer (on
Windows 10, it is under ``System Properties`` --> ``Advanced``) and add that
directory to the ``Path`` environment variable, using the GUI to edit path
segments.

Example segments should look like ``%APPDATA%\Python\Python3x\Scripts``, where
you have your version of Python instead of ``Python3x``.

You may need to restart your command prompt session to load the environment
variables.

.. seealso::
    See `Configuring Python (on Windows)
    <https://docs.python.org/3/using/windows.html#configuring-python>`_ for full
    details.

**Unix on Windows**


You may also install  `Windows Subsystem for Linux <https://msdn.microsoft.com/en-us/commandline/wsl/install-win10>`_
or `GNU utilities for Win32 <http://unxutils.sourceforge.net>`_ to use Unix commands on Windows.

Packaging tools
^^^^^^^^^^^^^^^

``pip`` and ``setuptools`` now come with Python 2 >=2.7.9 or Python 3 >=3.5. See the Python Packaging Authority's (PyPA) documentation `Requirements for Installing Packages <https://packaging.python.org/en/latest/installing/#requirements-for-installing-packages>`_ for full details.


Install DocSwitch
-----------------

At the command line:

.. code-block:: bash

    $ pip install --user doc_switch

Once the conda-forge channel has been enabled, cookiecutter can be installed with:

.. code-block:: bash

    $ conda install cookiecutter
