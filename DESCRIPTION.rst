About
------

* Contributors: `Nathan Printz <https://github.com/nprintz>`_ and `Geoff Rhodes <https://github.com/geoffrhodes>`_  
* `Full documentation on Read The Docs <http://jaide.readthedocs.org/>`_
* `Jaide Github <https://github.com/NetworkAutomation/jaide>`_  
* `Jaide GUI Github <https://github.com/NetworkAutomation/jaidegui>`_  
* `Pypi Page <https://pypi.python.org/pypi/jaide>`_
* `OSX/Windows Compiled Versions <https://github.com/NetworkAutomation/jaidegui/releases/latest>`_  

Description
------------

The ``jaide`` package contains two parts: a class library for developers (here called Jaide), and a CLI tool for network engineers (referred to as the CLI tool). The function of the Jaide class is to allow an engineer or developer to create and use a Jaide object for manipulating Junos devices. Similarly, the CLI tool can be used to manipulate or retrieve information/files/output from one or many devices. Not surprisingly, the CLI tool uses the Jaide class for its internal operations. Some features of both Jaide and the CLI tool include being able to poll devices for interface errors, grab basic system information, send any operational mode commands, send and commit a file containing a list of set commands, copy files to/from devices, get a configuration diff between two devices, perform a commit check, and run shell commands. A full list of features and their usage is available in the `documentation <http://jaide.readthedocs.org/>`_.

There is also a GUI available that wraps the CLI tool. More on it can be found at the `Jaide GUI github page <https://github.com/NetworkAutomation/jaidegui>`_.

Jaide, and therefore the CLI tool and the Jaide GUI, leverage several connection types to JunOS devices using python, including: ncclient, paramiko, and scp. With this base of modules, our goal is the ability to perform as many functions that you can do by directly connecting to a device from a remote interface (either Jaide object, or the CLI tool). Since we can do these remotely from one interface, these functions apply rapidly against multiple devices very easily. The CLI tool leverages multiprocessing for handling multiple connections simultaneously. Pushing code and upgrading 20 devices is quite a simple task with the Jaide tool in hand. 

**NOTE** This tool is most beneficial to those who have a basic understanding of JUNOS. This tool can be used to perform several functions against multiple Juniper devices running Junos very easily.  Please understand the ramifications of your actions when using this script before executing it. You can push very significant changes or CPU intensive commands to a lot of devices in the network from one command or GUI execution. This tool should be used with forethought, and we are not responsible for negligence, misuse, time, outages, damages or other repercussions as a result of using this tool.  

Installation
-------------

The easiest method to use to install jaide is through pip::

	pip install jaide

You can also download the source code from `github <https://github.com/NetworkAutomation/jaide>`_ and install it manually::

	python setup.py install

The above command is executed from the top level directory of the source distribution.