
gcc-1.37.1 for MINIX 1.5 386

This directory contains binaries sources and patches for gcc 1.37.1 
to it them to be compiled and run under MINIX 1.5.10
with Bruce Evans' 386 patches.
 
These are available from:

nmrdc1.nmrdc.nnmc.navy.mil [131.158.60.10]: /pub/minix/gcc-pc

The patches will allow compilation with Richard Tobin's port
of gcc (which this builds).  

The following files are included

16bcompress     A Minix-386 executable that can uncompress 16bit compressed
                files
README          this file
UPGRADING       Notes on how these may be up graded to later versions
                of GNU software
bashdiff.tar.Z  Diffs for bash-1.05
binutils.tar.Z  GNU bin utils source for Minix-386, and conversion
                program for changing GNU a.out format to Minix-386 a.out
emacsdif.tar.Z  Diffs for emacs-18.55
gasdiff.tar.Z   Diffs for gas-1.37
gcc.test        Simple test information for the installation
gccbin.tar.Z    Gcc binaries for Minix-386
gccdiff.tar.Z   Patches to gcc-1.37.1 to allow compilation un Minix-386
gccinc.tar.Z    Include files for gcc
gcclib.tar.Z    Minix-386 gcc compiled libraries
gdbdiff.tar.Z   Patches to gdb-386 to allow it to compile and run under
                Minix-386 (needs gnutoo patches)
gnutoo.tar.Z    Optional patches to allow Minix-386 to run gnu a.out files
                directly
libdiff.tar.Z   Patches to Minix libraries to allow gcc compilation
makediff.tar.Z  Patches for make-1.57
pmldiff.tar.Z   Patches for Fred Fish's portable math library

Instructions for installation are given in each tar file.  To unpack
any of the above type

    zcat <file> | tar xvf -

This file create a subdirectory in the current directory with the
unpack files in it.  If you don't have a 16bit uncompress use the 
provided 16bcompress

    cat <file> | 16bcompress -d | tar xvf -

There is also a subdirectory which includes the original (unpatched
sources) to which the above patches apply

bash1.05.tar.Z  GNU Bourne Again SHell version 1.05
bash.pat.tar.Z  Official Patches to bash-1.05
gas-1.37.tar.Z  GNU Assembler 1.37
gcc1.371.tar.Z  GNU C compiler 1.37.1
gdb-3.5.tar.Z   GNU source level debugger
make3.57.tar.Z  GNU Make
pml.tar.Z       Portable math library (libm.a)
estdio21.tar.Z  Earl Chew's replacement stdio library


If you don't wish to re-compile the distributed binaries are perfectly
ok to use.  In this case you need only unpack and install gccbin
gccinc and gcclib -- which you will have to do anyway before you can
recompile anything.

A small patch to the Minix-386 kernel is necessary for floating point
to be emulated properly if you do not have a 387.  The floating point
is adequate but hacky and should be replaced.

No guarantee is given with these patches, but I hope you find them
useful.  If you find any bugs please let us know but we don't
guarantee we'll have the time to fix them.

Note that I (awb@ed.ac.uk) no longer use Minix regularly and am likely
to use it less in the future so I am unlikely to upgrade these.  But I
am willing to answer technical questions about upgrading.

Thanks go to:
     Richard Stallman and FSF for the GNU software
     Andy Tanenbaum for MINIX
     Bruce Evans for his 386 patches
     Earl Chew for estdio
     Fred Fish for pml
     Richard Tobin for doing the difficult bits
     Dept of AI and AIAI, University of Edinburgh for 
       providing machines used in bootstraping this software.
     And others who I have forgotten (sorry).


Alan W Black   awb@ed.ac.uk
Richard Tobin  richard@aiai.ed.ac.uk
March 1991
(updated June 1992)
      
