%title: Cyberspectrum March 18 2015 -- Is Software Radio really that hard?
%author: Martin Braun <martin.braun@ettus.com>
%date: 2015-03-18

-> The SDR Mythbusters -- Is SDR really that hard? <-
=====================================================

* How hard is it to build radio apps?
* Is GNU Radio difficult?
* Which tools do we have to make SDR easier?


     ___ _   _
    | __| |_| |_ _  _ ___                        O
    | _||  _|  _| || (_-<                 O      |      O
    |___|\__|\__|\_,_/__/          O      |      |      |
                                   |      |      |      |
    =========================O====================================>
     |     |     |     |        ___                         _
     |     |     |     O       | _ \___ ___ ___ __ _ _ _ __| |_
     O     |     O             |   / -_|_-</ -_) _` | '_/ _| ' \
           O                   |_|_\___/__/\___\__,_|_| \__|_||_|


-------------------------------------

-> A clean slate <-
=================================


           Page deliberately left blank

-------------------------------------

-> Step One: Getting GNU Radio <-
=================================

* Easiest starting point: The GNU Radio Live DVD
* Still easy: `apt-get install gnuradio` (or `yum install gnuradio` or whatever)
* Packages available for Debian, Ubuntu, Fedora, Gentoo and probably many more
* Or of course... a source build
* It may be as simple as:

    cmake ..
    make
    make install

* Or even easier using PyBOMBS

-------------------------------------------

-> PyBOMBS -- The apt-get of GNU Radio <-
=========================================

* Available at: http://gnuradio.org/pybombs
* Still heavily under development
* Facilitates installing GNU Radio in your home directory
    - Helps you set up environment variables etc.
* Comes with an app store (graphics!)
* Modules are added by PyBOMBS maintainers in form of lightweight recipes

    # gr-specest: A spectrum estimation module
    category: common
    depends: gnuradio
    source: git://https://github.com/kit-cel/gr-specest.git
    gitbranch: 37
    inherit: cmake

* Allows easy access for community members to contribute
* But which modules are there?

----------------------------------------------

-> CGRAN -- The Comprehensive GNU Radio Archive Network <-
==========================================================

* Spiritual Cousin of CTAN, CPAN...
* Easy access to the entire free & open software radio ecosystem
* Automatically generated website listing all OOT modules
* Between CGRAN and PyBOMBS, finding and installing modules should be a simple task


* CGRAN used to be hosted by George Nychis (Thanks!)
* Currently being overhauled by the PyBOMB squad
* Fully auto-generated, directly tied into PyBOMBS

----------------------------------------------

-> Actually getting started: Official Tutorials <-
==================================================

* Find these online at:
    - http://gnuradio.org/redmine/projects/gnuradio/wiki/Guided_Tutorials
* Comes with a free set of codes: `gr-tutorial`

----------------------------------------------

-> The GNU Radio Companion (GRC) <-
====================================

* Ignore GRC at your own peril!
* Comes with fine instrumentation tools
* Read the Python output for further understanding

----------------------------------------------

-> Where do I learn about these blocks? <-
===========================================

* Read our fine manual!
    - http://gnuradio.org/doc/
* All blocks are browsable through several paths, and searchable
* GRC provides docs

----------------------------------------------

-> `gr_modtool` -- The Swiss Army Knife of module manipulation <-
=================================================================

* Modify and create your OOTs from the command line
    - Unfortunately, only the command line at this time

    List of possible commands:
    
    Name      Aliases          Description
    =====================================================================
    disable   dis              Disable block (comments out CMake entries for files) 
    info      getinfo,inf      Return information about a given module 
    remove    rm,del           Remove block (delete files and remove Makefile entries) 
    makexml   mx               Make XML file for GRC block bindings 
    add       insert           Add block to the out-of-tree module. 
    newmod    nm,create        Create a new out-of-tree module 
    rename    insert           Add block to the out-of-tree module. 
    =====================================================================

----------------------------------------------

-> Writing blocks: A core skill of developing SDR <-
====================================================

* `gr_modtool` tries to make this as easy as possible
* Languages available:
    - Python, for fast & easy dev
    - C++, for higher performance

----------------------------------------------

-> Where do I figure out how to configure/code all these blocks? <-
===================================================================

* How do learn how to do all this wireless communications stuff?
* Which codez do I put into my `<+ do signal processing here +>`?

* Well...

----------------------------------------------

-> Getting Help -- Interacting with other People <-
===================================================

* discuss-gnuradio, usrp-users mailing lists
    - Very responsive!
* IRC: #gnuradio on Freenode

* Join the discussions!
* But read this first:
    - http://gnuradio.org/redmine/projects/gnuradio/wiki/ReportingErrors

----------------------------------------------

-> Improving GNU Radio <-
=========================

* You've found a bug? Something's bothering you?
* Fix it!
    - Actual bugs
    - Missing features
    - Bad docs
    - Unintuitive coding


----------------------------------------------

-> Am I supposed to do this all alone, and without clothes? <-
===============================================================

* No!
* See fan shop
* But, most importantly, join the community
* We have a conference! (Probably end of August)
* Local meetings

----------------------------------------------

-> Conclusion <-
================


* SDR is infinitely hard
* But that shouldn't stop you
* And most of the tools aren't that bad
