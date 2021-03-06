- 👋 Hi, I’m @KingEther666
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
KingEther666/KingEther666 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
Google Git
Switch user
Sign out
‪jacoby robbie‬ <robbiejacoby36@gmail.com>
android / platform / external / grub / refs/heads/gingerbread / . / INSTALL
blob: 1ba68a6905f50d7bba4b51c041fa4c7b0cb01505 [file] [log] [blame]
-*- Text -*-
This is the GRUB.  Welcome.
This file contains instructions for compiling and installing the GRUB.
The Requirements
================
GRUB depends on some software packages installed into your system. If
you don't have any of them, please obtain and install them before
configuring the GRUB.
* GCC
  Probably every recent GCC should work, but we recommend GCC 2.95 and
  later, since you can create smaller binary images. See the web page
  <http://gcc.gnu.org/>.
* GNU Make
  For now, the Makefiles produced by Automake depends on GNU Make. See
  the web page <http://www.gnu.org/software/make/make.html>.
* GNU binutils 2.9.1.0.23 or later
  Binutils has changed the behavior of 16bit assembler between 2.9.1
  and 2.9.1.0.x, and we support only 2.9.1.0.x and higher. In
  particular, we recommend using binutils 2.10, since it is the only
  public release that supports real 16bit mode. Please take a look at
  the web page <http://sourceware.cygnus.com/binutils/>, for more
  information. Note that you don't have to install it into any system
  directory. See the section "Operation Controls", if you want to
  install binutils into your own directory.
If you'd like to develop GRUB, these below are also required. Don't
forget to specify the option `--enable-maintainer-mode' when running the
configure script.
* Texinfo 4.0 or later
  We use some new macros in the documents, so you need a recent
  Texinfo release. See the web page
  <http://www.gnu.org/software/texinfo/texinfo.html>.
* Developers: GNU Autoconf 2.5x and GNU Automake 1.7 or later
  You should not need Automake just to compile GRUB, but you will need
  it if you edit any of the build files (Makefile.am, configure.in,
  etc).  We use the new "per-executable flags" feature found in the
  latest release of automake.  See the web page
  <http://www.gnu.org/software/automake/automake.html>.
Configuring the GRUB
====================
The `configure' shell script attempts to guess correct values for
various system-dependent variables used during compilation.  It uses
those values to create a `Makefile' in each directory of the package.
It may also create one or more `.h' files containing system-dependent
definitions.  Finally, it creates a shell script `config.status' that
you can run in the future to recreate the current configuration, a
file `config.cache' that saves the results of its tests to speed up
reconfiguring, and a file `config.log' containing compiler output
(useful mainly for debugging `configure').
If you need to do unusual things to compile the package, please try to
figure out how `configure' could check whether to do them, and mail
diffs or instructions to the address given in the `README' so they can
be considered for the next release.  If at some point `config.cache'
contains results you don't want to keep, you may remove or edit it.
The file `configure.in' is used to create `configure' by a program
called `autoconf'.  You only need `configure.in' if you want to change
it or regenerate `configure' using a newer version of `autoconf'.
Building the GRUB
=================
The simplest way to compile this package is:
  1. `cd' to the directory containing the package's source code and
     type `./configure' to configure the package for your system.  If
     you're using `csh' on an old version of System V, you might need
     to type `sh ./configure' instead to prevent `csh' from trying to
     execute `configure' itself.
     Running `configure' takes awhile.  While running, it prints some
     messages telling which features it is checking for.
  2. Type `make' to compile the package.
  3. Optionally, type `make check' to run any self-tests that come with
     the package.
  4. Type `make install' to install the programs and any data files and
     documentation.
  5. You can remove the program binaries and object files from the
     source code directory by typing `make clean'.  To also remove the
     files that `configure' created (so you can compile the package for
     a different kind of computer), type `make distclean'.  There is
     also a `make maintainer-clean' target, but that is intended mainly
     for the package's developers.  If you use it, you may have to get
     all sorts of other programs in order to regenerate files that came
     with the distribution.
Compiling For Multiple Architectures
====================================
You can compile the package for more than one kind of computer at the
same time, by placing the object files for each architecture in their
own directory.  `cd' to the directory where you want the object files
and executables to go and run the `configure' script.  `configure'
automatically checks for the source code in the directory that
`configure' is in and in `..'.
Installation Names
==================
By default, `make install' will install the package's files in
`/usr/local/bin', `/usr/local/man', etc.  You can specify an
installation prefix by giving `configure' the option `--prefix=PATH'.
You can specify separate installation prefixes for
architecture-specific files and architecture-independent files.  If
you give `configure' the option `--exec-prefix=PATH', the package will
use PATH as the prefix for installing programs and libraries.
Documentation and other data files will still use the regular prefix.
In addition, if you use an unusual directory layout you can give
options like `--bindir=PATH' to specify different values for
particular kinds of files.  Run `configure --help' for a list of the
directories you can set and what kinds of files go in them.
If the package supports it, you can cause programs to be installed
with an extra prefix or suffix on their names by giving `configure'
the option `--program-prefix=PREFIX' or `--program-suffix=SUFFIX'.
Please note, however, that the GRUB knows where it is located in the
filesystem.  If you have installed it in an unusual location, the
system might not work properly, or at all.  The chief utility of these
options for the GRUB is to allow you to "install" in some alternate
location, and then copy these to the actual root filesystem later.
Sharing Defaults
================
If you want to set default values for `configure' scripts to share,
you can create a site shell script called `config.site' that gives
default values for variables like `CC', `cache_file', and `prefix'.
`configure' looks for `PREFIX/share/config.site' if it exists, then
`PREFIX/etc/config.site' if it exists.  Or, you can set the
`CONFIG_SITE' environment variable to the location of the site script.
A warning: not all `configure' scripts look for a site script.
Operation Controls
==================
   `configure' recognizes the following options to control how it
operates.
`--cache-file=FILE'
     Use and save the results of the tests in FILE instead of
     `./config.cache'.  Set FILE to `/dev/null' to disable caching, for
     debugging `configure'.
`--help'
     Print a summary of the options to `configure', and exit.
`--quiet'
`--silent'
`-q'
     Do not print messages saying which checks are being made.
`--srcdir=DIR'
     Look for the package's source code in directory DIR.  Usually
     `configure' can determine that directory automatically.
`--version'
     Print the version of Autoconf used to generate the `configure'
     script, and exit.
`--enable-maintainer-mode'
     Enable make rules and dependencies not useful (and sometimes
     confusing) to the casual installer. If you are a GRUB developer,
     it is a good idea to specify this option.
`--disable-ext2fs'
     Omit the ext2fs support in Stage 2.
`--disable-fat'
     Omit the FAT support in Stage 2.
`--disable-ffs'
     Omit the FFS support in Stage 2.
`--disable-minix'
     Omit the Minix fs support in Stage 2.
`--disable-reiserfs'
     Omit the ReiserFS support in Stage 2.
`--disable-vstafs'
     Omit the VSTa filesystem support in Stage 2.
`--disable-jfs'
     Omit the JFS support in Stage 2.
`--disable-xfs'
     Omit the XFS support in Stage 2.
`--disable-ufs2'
     Omit the UFS2 support in Stage 2.
`--disable-iso9660'
     Omit the ISO9660 support in Stage 2.
`--disable-gunzip'
     Omit the decompression support in Stage 2.
`--disable-md5-password'
     Omit the MD5 password support in Stage2.
`--with-binutils=PATH'
     Search the path PATH to find binutils. If you have installed your
     binutils executables into an unusual location where GCC doesn't
     search by default, use this option.
`--without-curses'
     Don't use the curses library.
`--disable-hercules'
     Omit the hercules console support in Stage 2.
`--disable-serial'
     Omit the serial terminal support in Stage 2.
`--enable-serial-speed-simulation'
     Simulate the slowness of a serial device in the grub shell. This
     option is useful for GRUB developers, as you can test the
     performance of a terminal emulation even on pseudo terminals.
`--enable-preset-menu=FILE'
     Preset a menu file FILE in Stage 2. This is useful, if you cannot
     put a configuration file on a filesystem for some reason (e.g. when
     you need to set the default terminal to a serial terminal in an
     embedded system).
`--enable-example-kernel'
     Build the example Multiboot kernel in the directory "docs". You
     will be able to boot the image "kernel" with GRUB.
`--disable-auto-linux-mem-opt'
     Don't pass the "mem=" option automatically, when booting Linux.
     You can also disable the feature at run time.
`configure' also accepts several options for the network support. See
the file `netboot/README.netboot', for more information.
Powered by Gitiles| Privacy
txt
json
