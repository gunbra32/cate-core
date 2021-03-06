=====
Setup
=====

System Requirements
===================

Hardware
--------

It is recommended to use an up-to-date computer, with at least 8GB of RAM and a multi-core CPU.
The most important bottlenecks will first be the data transfer rate from local data caches into the
executing program, so it is advised to use fast solid state disks. Secondly, the internet connection
speed matters, because the CCI Toolbox will frequently have to download data from remote services
in order to cache it locally.

Operating Systems
-----------------

The CCI Toolbox is supposed to work on up-to-date Windows, Mac OS X, and Linux operating systems.


Installation
============

Using the Installers
--------------------

Installers for the Linux, Mac OS X, and Windows platform can be downloaded from the project's
`release page <https://github.com/CCI-Tools/cate-core/releases>`_ on GitHub.

The installers are self-contained, so there is no need to install additional software to run the
CCI Toolbox.

The CCI Toolbox installers for all platforms are currently
customized `Anaconda <https://www.continuum.io/why-anaconda>`_ installers. In the following we provide some notes
regarding its usage on Windows and Unix/Darwin systems.


**Windows Installer**


When you run the installer on Windows, make sure you un-check **Add Anaconda to my PATH environment variable**.
Otherwise the Anaconda Python distribution used by the CCI Toolbox would become your system's default Python.

.. figure:: ../_static/figures/installer-win.png
   :scale: 100 %
   :align: center


**Linux/Darwin Installers**


On Linux/Darwin systems, the downloaded installer is a shell script. To run it, open a terminal window,
``cd`` into the directory where you've downloaded the installer and execute the shell script.

.. code-block:: console

    $ cd ~/Downloads
    $ ./cate-0.6.0-Linux-x86_64.sh

If the installer script is not yet executable, type:

.. code-block:: console

    $ chmod +x cate-0.6.0-Linux-x86_64.sh

By default, the installer will install the CCI Toolbox into ``~/cate``. If you want it in another location, use the
``-p`` (=prefix) option, e.g.

.. code-block:: console

    $ ./cate-0.6.0-Linux-x86_64.sh -p cci-toolbox

Use the ``-h`` option to display other install options.


Installing from Sources
-----------------------

If you are a developer you may wish to build and install the CCI Toolbox from Python sources.
In this case, please follow the instructions given in the project's
`README <https://github.com/CCI-Tools/cate-core/blob/master/README.md>`_ on GitHub.


Configuration
=============

CCI Toolbox' configuration file is called ``conf.py`` and is located in the ``~/.cate`` directory, where ``~`` is
the current user's home directory.

Given here is an overview of the possible configuration parameters (currently only one):

:``data_stores_path``:
    Directory where Cate stores information about data stores and also saves local data files synchronized with their
    remote versions. Use the tilde '~' (also on Windows) within the path to point to your home directory.
    This directory can become rather populated once after a while and it is advisable to place it where there exists
    a high transfer rate and sufficient capacity. Ideally, you would let it point to a dedicated solid state disc (SSD).
    The default value for ``data_stores_path`` is the ``~/.cate/data_stores`` directory.


