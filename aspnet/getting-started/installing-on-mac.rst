Installing ASP.NET 5 On Mac OS X
================================

By `Steve Smith`_

ASP.NET 5 runs on the .NET Execution Environment (DNX), which is available on multiple platforms, including OS X. This article describes how to install DNX, and therefore ASP.NET 5, on OS X, using `Homebrew <http://brew.sh/>`_. 

In this article:
	- `Install ASP.NET 5 on OS X`_

Install ASP.NET 5 on OS X
-------------------------

Install Mono
^^^^^^^^^^^^

Currently, ASP.NET 5 on OS X requires the `Mono <http://mono-project.com>`_ runtime. Mono is an ongoing effort to port the .NET Framework to other platforms. It is one of the ways .NET applications can run on platforms other than Windows.

You can install the latest version of Mono from the `Mono project downloads page <http://www.mono-project.com/download/>`_, just select Mac OS X and click download. The latest version should be compatible with ASP.NET 5 (specifically, you need at least Mono 4.0.1). Alternatively, if you use the `Homebrew <http://brew.sh>`_ package manager, you can install mono using the following command::

	brew install mono
	
Installing DNVM
^^^^^^^^^^^^^^^

Next, you need to install the .NET Version Manager (DNVM). You can do so by running the following installation script::

	curl -sSL https://raw.githubusercontent.com/aspnet/Home/master/dnvminstall.sh | sh && source ~/.dnx/dnvm/dnvm.sh

Alternatively, you can manually install it by downloading the ?? file from the `aspnet/Home <https://github.com/aspnet/Home>`_ repository and place it in the ?? directory on your file system. Then, add the following lines to your shell startup script::

	<shell lines>
	
Next, run ``dnvm`` to verify that your terminal understands this command. If it does not, run the command ``source dnvm.sh`` to link it, then try running ``dnvm`` again. You should see something like this:

.. image:: installing-on-mac/_static/run-dnvm.png

Installing DNX
^^^^^^^^^^^^^^

To install the latest version of DNX using DNVM, run: 

``dnvm upgrade``

Now that DNX is installed, you're ready to begin using ASP.NET 5! Learn how you can :doc:`create a cross-platform console application </dnx/console>` or a simple ASP.NET MVC application that runs within DNX.

.. TODO: create links to cross-platform console application and simple ASP.NET MVC application running in DNX/command line.

Summary
-------

ASP.NET 5 is built on the cross-platform .NET Execution Environment, which can be installed on OS X as well as Linux and Windows. Installing DNX and ASP.NET 5 on OS X takes just a few minutes, using a few Terminal commands. 

Related Resources
-----------------

- :doc:`Installing ASP.NET 5 on Windows <installing-on-windows>`
- :doc:`Your First ASP.NET 5 Application Using Visual Studio </tutorials/your-first-aspnet-application>`

