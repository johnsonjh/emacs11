EMACS-11
========

1. Well folks, you asked for it and here it is.  Unfortunately, it has been a couple years since I used any of this stuff, so I'm a little rusty about what the various pieces are.  The following represents my best guess, going from memory, and looking at some of the pieces.

2. The following are considered to be a minimal usable distribution suitable for transmission over the net.  Note that there are two distinct flavors, one for *VAX* using *VT100*, and one for *PDP-11* using *VT52*.

File | Size | Usage
--- | --- | ---
`README | xxxxx | This file.
`emacs.txt` | 10659 | "*Quick reference*" guide to **EMACS-11** commands.
`emacs.doc` | 65034 | **EMACS-11** documentation ready for printing.
`emacs.src` | 61032 | **EMACS-11** macro source file.  Use "`vaxbld.tec`" to compact into an executable macro file "`emacs.tec`". Use on *VAX*/*VMS* with *VT100*'s.
`vaxbld.tec` | 1615 | Used to compact "`emacs.src`" file into executable macro file "`emacs.tec`". Use on *VAX*/*VMS* with *VT100*.
`emacs11.tec` | 61166 | Slightly modified version of "`emacs.src`". Use "`bldemacs.tec`" to compact into executable macro file "`teco.tec`". Use on *PDP-11*'s with *VT52*'s.
`bldemacs.tec` | 1558 | **TECO** command file to compact the **EMACS-11** macro source file "`emacs11.tec`" into an executable **TECO** macro file "`teco.tec`" by removing all extraneous characters.  Use on *PDP-11*'s.

3. The following files are available in the tape distribution only:

File | Size | Usage
--- | --- | ---
`MITemacs.doc` | 666989 | Machine readable form of **EMACS** documentation for the *TOPS-20* version of **EMACS**.  (Available on tape distribution only)
`ema.odl` | 1183	Some kind of command file for one of the DEC operating systems. (I told you I was rusty!!!)
`ema.tkb` | 2778	Command file for building **TECO** under *RSX-11* and/or *VAX*/*VMS*
`emacs.rno` | 54116 | **EMACS-11** manual in *RUNOFF* form.
`emacs.tec` | 4941 | Compacted form of `emacs.src`
`emacs11.doc` | 40088 | Earlier form of `emacs.doc`
`teco.doc` | 711649 | Machine readable form of documentation for **TECO**.
`teco.tec` | 4915 | Compacted form of `emacs11.tec`
`tioasm.cmd` | 497 | Another mysterious command file

4. Some possibly helpful hints.

I seem to remember that the **TECO** source was modified slightly to look for "`teco.tec`" (or whatever you want to call the compacted macro file) in a special startup directory.  Thus, when the **TECO** executable was copied to "`ema`", and invoked with the name "`ema`", it would automatically start up with the compacted macro file, otherwise, you would get normal **TECO**.  It is possible to load the compacted macro file manually and start it up by hand each time, but I forget the exact procedure.

I think there are a couple terminal dependencies wired into the macro package, one for *VT52*, and one for *VT100*.

There were some problems with *VMS* trapping certain control characters that I was never able to completely fix.

The macro sources are in "**Structured _TECO_**" (and I'll bet you thought **TECO** was an editor instead of a programming language!!).

Note that there are a couple embedded *ESCAPE* characters near the end of the macro source files "`emacs11.tec`" and "`emacs.src`".

**HAVE FUN AND GOOD LUCK.**

```text
Fred Fish
UniSoft Systems Inc,
Berkeley, Ca
1-415-644-1230 ext 242
```
