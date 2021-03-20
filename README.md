# ScotKirvan/FreeWPC fork (yeah, I changed the capitalization of the repo's name)

## 2021/03/15 
This repo hasn't been active for quite a long time.  I'm looking into 
using it in conjunction with another project I'm developing, so I've started investigating
what it's going to take to get all these pieces (FreeWPC to create ROMS, VPinMAME to run 
them, and our Unreal plugin to implement the virutal tables) up and running together.

For now, I'm just going to try to get the repository updated a bit, and 
as I do my research I'll drop notes here.

The links on the site point to oddchnage.com/freewpc, which doesn't 
exist any longer. There is an
[archived version](https://web.archive.org/web/20110929084558/http://www.oddchange.com/freewpc/)
which may be older than the repository code.  The FAQ and other documentation 
may prove useful.

This looks GREAT! A 2011 [Google Code](https://code.google.com/archive/p/freewpc/wikis/UbuntuGCC6809Install.wiki)
 archive which describes the process of creating GCC6809
(a cross-compiler for the Motorolla 6809 chipset) on Ubuntu - specifically for FreeWPC.
This site looks like a great source of information.  UPDATE 20210319 - I tried this - it was looking so promising,
but I was building in WSL Ubuntu 18.04.  Everything up to the patch went great and it all looked very promising,
but building the patched source failed.  I'm guessing it's because of changes in more modern C++ versions.  C++ was,
at best, at version 10 in 2010 (currently, it's V17), so we may need to roll back to an older ubuntu or 
find some other way to build with an older c++.  This sounds like a ideal reason for a Docker container - haha!

[Flippers.be](https://www.flippers.be/freewpc.html) looks to be another good resource.  It has a 
step-by-step explanation of how to start with an empty ROM and piece by piece, add functionality.
It's also where I learned the history of the repo:  "Around 2010 there was a lot of activity and 
several people involved. The main programmer (Brian) has stopped all work when he started to work 
for Heighway Pinball. Since then there are no updates anymore to the master git resource."



---
# Original README

This is FreeWPC, an open source operating system for the Williams
Pinball Controller (WPC) family of pinball machines.  FreeWPC is
licensed under the GNU General Public License, Version 2.

The sources for the core routines are located in 'kernel';
other common code is in 'common', and game-specific code can be found 
in a subdirectory based on the machine name, under 'machine'.
There are also a number of tools included with the distribution
for generating some of the source code and for building ROM images
that are under 'tools'.

You will also need several tools not here in order to build.
See the file doc/build.html for more detailed information.  Most
importantly, you'll need a copy of the gcc6809 cross-compiler.
Many standard UNIX utilities are needed as well.  FreeWPC has been
built successfully on Linux and Cygwin.

Email suggestions/comments/questions to <brian@oddchange.com>.

Visit the homepage at http://www.oddchange.com/freewpc for more
information.

