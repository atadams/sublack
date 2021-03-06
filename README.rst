.. image:: https://travis-ci.org/jgirardet/sublack.svg?branch=master
    :target: https://travis-ci.org/jgirardet/sublack


===============================
sublack
===============================


`Black`_ integration for SublimeText


* License : GNU General Public License v3 or later (GPLv3+) 
* Source: https://github.com/jgirardet/sublack



Usage
--------

* Run Black on current file:
	Press `Ctrl-Alt-B` to format the entire file.
	You can also `Ctrl-Shift-P` (Mac: `Cmd-Shift-P`) and select `Sublack: Format file`.


* Run Black with --diff:
	Press `Ctrl-Alt-Shift-B` will show diff in a new tab.
	You can also `Ctrl-Shift-P` (Mac: `Cmd-Shift-P`) and select `Sublack: Diff file`.




Installation
-------------

#. Install `Black`_ (if you haven't already)::
   
	   pip install black # Requires python 3.6

#. In PackageControl just find ``sublack``, and that's it !

or

Without PackageControl  install manually by navigating to Sublime's `Packages` folder and cloning this repository::

      git clone https://github.com/jgirardet/sublack.git

Settings
---------

* black_black_command:
	Set custom location. Default = "black".

* black_on_save:
	Black is always run before saving file. Default = false.

* black_line_length:
	Set custom line length option used by `Black`_. Default = null which lets black default.

* black_fast:
	Black fast mode. default is false.

* black_debug_on:
	Show non error messages in console. Default = false. Error messages are always shown in console.

* black_default_encoding:
	Should not be changed. Only needed on some OSX platforms.


Issues
---------

If there is something wrong with this plugin, `add an issue <https://github.com/kgirardet/sublack/issues>`_ on GitHub and I'll try to address it.


Thanks
----------

This plugin is very inspired by the very good `PyYapf <https://github.com/jason-kane/PyYapf>`_ Plugin. Thanks to Jason Kane.

Changelog
-----------

1.6.0:
	- Change keymaps from `f` to `b` (like black oO) due to conflict with Anaconda.
	- Change installation instruction to use Packagecontrol.
1.5.0:
	- All settings are now prefixed with `black_`
	- use on_pre_save_async
	- and various fix (`#7061 <https://github.com/wbond/package_control_channel/pull/7061>`_, thanks to `Thom1729  <https://github.com/Thom1729 >`_)
1.4.1:
	- add tests
	- Improve Settings menu entry and add Key Bindings menu entry(`#9 <https://github.com/jgirardet/sublack/pull/9>`_, thanks to `catch22 <https://github.com/catch22>`_)
1.4.0:
	- add black_diff command
	- add black_diff keymap
	- add fast setting
	- refactor code
	- do nothing if already formated and show "already formated" in statusbar
1.3.4:
	- Format sublack with Black (`#8 <https://github.com/jgirardet/sublack/pull/8>`_, thanks to `mschneiderwind <https://github.com/mschneiderwind>`_)
1.3.3:
	- Fix encoding if not given by SublimeText.
1.3.2:
	- BugFix : Click library Bug with locale under OSX
1.3.1:
	- update README
1.3.0:
	- use '-' argument to format inline document wihout saving it
	- consequently post-save became pre-save
	- line_length typo in settings
	- add log
1.2.0:
	- add error handling (thanks to `nicokist <https://github.com/nicokist>`_)
1.1.0:
	- add line_length option
1.0.0:
	- make plugin
	- add on_save option

.. _Black : https://github.com/ambv/black 