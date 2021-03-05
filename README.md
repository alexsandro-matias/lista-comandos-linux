# Lista de Comandos Linux com seus Respectivos parâmetros

## Comandos Básicos

 * [**ls**](#ls)
 * [**cd**](#cd)
 * [**mkdir**](#mkdir)

<a id="ls"></a>
## ls
Lista arquivos num determinado diretório.

NAME
       ls - list directory contents

SYNOPSIS
       ls [OPTION]... [FILE]...

DESCRIPTION
       List information about the FILEs (the current directory by default).  Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.

       Mandatory arguments to long options are mandatory for short options too.

       -a, --all
              do not ignore entries starting with .

       -A, --almost-all
              do not list implied . and ..

       --author
              with -l, print the author of each file

       -b, --escape
              print C-style escapes for nongraphic characters

       --block-size=SIZE
              with -l, scale sizes by SIZE when printing them; e.g., '--block-size=M'; see SIZE format below

       -B, --ignore-backups
              do not list implied entries ending with ~

       -c     with -lt: sort by, and show, ctime (time of last modification of file status information); with -l: show ctime and sort by name; otherwise: sort by ctime, newest first

       -C     list entries by columns

       --color[=WHEN]
              colorize the output; WHEN can be 'always' (default if omitted), 'auto', or 'never'; more info below

       -d, --directory
              list directories themselves, not their contents

       -D, --dired
              generate output designed for Emacs' dired mode

       -f     do not sort, enable -aU, disable -ls --color

       -F, --classify
              append indicator (one of */=>@|) to entries

       --file-type
              likewise, except do not append '*'

       --format=WORD
              across -x, commas -m, horizontal -x, long -l, single-column -1, verbose -l, vertical -C

       --full-time
              like -l --time-style=full-iso

       -g     like -l, but do not list owner

       --group-directories-first
              group directories before files;

              can be augmented with a --sort option, but any use of --sort=none (-U) disables grouping

       -G, --no-group
              in a long listing, don't print group names

       -h, --human-readable
              with -l and -s, print sizes like 1K 234M 2G etc.

       --si   likewise, but use powers of 1000 not 1024

       -H, --dereference-command-line
              follow symbolic links listed on the command line

       --dereference-command-line-symlink-to-dir
              follow each command line symbolic link

              that points to a directory

       --hide=PATTERN
              do not list implied entries matching shell PATTERN (overridden by -a or -A)

       --hyperlink[=WHEN]
              hyperlink file names; WHEN can be 'always' (default if omitted), 'auto', or 'never'

       --indicator-style=WORD
              append indicator with style WORD to entry names: none (default), slash (-p), file-type (--file-type), classify (-F)

       -i, --inode
              print the index number of each file

       -I, --ignore=PATTERN
              do not list implied entries matching shell PATTERN

       -k, --kibibytes
              default to 1024-byte blocks for disk usage; used only with -s and per directory totals

       -l     use a long listing format

       -L, --dereference
              when showing file information for a symbolic link, show information for the file the link references rather than for the link itself

       -m     fill width with a comma separated list of entries

       -n, --numeric-uid-gid
              like -l, but list numeric user and group IDs

       -N, --literal
              print entry names without quoting

       -o     like -l, but do not list group information

       -p, --indicator-style=slash
              append / indicator to directories

       -q, --hide-control-chars
              print ? instead of nongraphic characters

       --show-control-chars
              show nongraphic characters as-is (the default, unless program is 'ls' and output is a terminal)

       -Q, --quote-name
              enclose entry names in double quotes

       --quoting-style=WORD
              use quoting style WORD for entry names: literal, locale, shell, shell-always, shell-escape, shell-escape-always, c, escape (overrides QUOTING_STYLE environment variable)

       -r, --reverse
              reverse order while sorting

       -R, --recursive
              list subdirectories recursively

       -s, --size
              print the allocated size of each file, in blocks

       -S     sort by file size, largest first

       --sort=WORD
              sort by WORD instead of name: none (-U), size (-S), time (-t), version (-v), extension (-X)

       --time=WORD
              change the default of using modification times; access time (-u): atime, access, use; change time (-c): ctime, status; birth time: birth, creation;

              with -l, WORD determines which time to show; with --sort=time, sort by WORD (newest first)

       --time-style=TIME_STYLE
              time/date format with -l; see TIME_STYLE below

       -t     sort by time, newest first; see --time

       -T, --tabsize=COLS
              assume tab stops at each COLS instead of 8

       -u     with -lt: sort by, and show, access time; with -l: show access time and sort by name; otherwise: sort by access time, newest first

       -U     do not sort; list entries in directory order

       -v     natural sort of (version) numbers within text

       -w, --width=COLS
              set output width to COLS.  0 means no limit

       -x     list entries by lines instead of by columns

       -X     sort alphabetically by entry extension

       -Z, --context
              print any security context of each file

       -1     list one file per line.  Avoid '\n' with -q or -b

       --help display this help and exit

       --version
              output version information and exit

       The SIZE argument is an integer and optional unit (example: 10K is 10*1024).  Units are K,M,G,T,P,E,Z,Y (powers of 1024) or KB,MB,... (powers of 1000).  Binary prefixes can be used, too: KiB=K, MiB=M, and so on.

       The  TIME_STYLE  argument  can  be  full-iso,  long-iso, iso, locale, or +FORMAT.  FORMAT is interpreted like in date(1).  If FORMAT is FORMAT1<newline>FORMAT2, then FORMAT1 applies to non-recent files and FORMAT2 to recent
       files.  TIME_STYLE prefixed with 'posix-' takes effect only outside the POSIX locale.  Also the TIME_STYLE environment variable sets the default style to use.

       Using color to distinguish file types is disabled both by default and with --color=never.  With --color=auto, ls emits color codes only when standard output is connected to a terminal.  The  LS_COLORS  environment  variable
       can change the settings.  Use the dircolors command to set it.



<a id="cd"></a>
## cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.
    
    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable.
    
    The variable CDPATH defines the search path for the directory containing
    DIR.  Alternative directory names in CDPATH are separated by a colon (:).
    A null directory name is the same as the current directory.  If DIR begins
    with a slash (/), then CDPATH is not used.
    
    If the directory is not found, and the shell option `cdable_vars' is set,
    the word is assumed to be  a variable name.  If that variable has a value,
    its value is used for DIR.
    
    Options:
      -L	force symbolic links to be followed: resolve symbolic
    		links in DIR after processing instances of `..'
      -P	use the physical directory structure without following
    		symbolic links: resolve symbolic links in DIR before
    		processing instances of `..'
      -e	if the -P option is supplied, and the current working
    		directory cannot be determined successfully, exit with
    		a non-zero status
      -@	on systems that support it, present a file with extended
    		attributes as a directory containing the file attributes
    
    The default is to follow symbolic links, as if `-L' were specified.
    `..' is processed by removing the immediately previous pathname component
    back to a slash or the beginning of DIR.
    
    Exit Status:
    Returns 0 if the directory is changed, 
    
    
    ## Compactadores e Arquivadores
 * [**gzip**](gzip)
 * [**zip**](#zip)

    
<a id="gzip"></a>
## gzip

NAME
       gzip, gunzip, zcat - compress or expand files

SYNOPSIS
       gzip [ -acdfhklLnNrtvV19 ] [-S suffix] [ name ...  ]
       gunzip [ -acfhklLnNrtvV ] [-S suffix] [ name ...  ]
       zcat [ -fhLV ] [ name ...  ]

DESCRIPTION
       Gzip  reduces the size of the named files using Lempel-Ziv coding (LZ77).  Whenever possible, each file is replaced by one with the extension .gz, while keeping the same ownership modes, access and modification times.  (The
       default extension is z for MSDOS, OS/2 FAT, Windows NT FAT and Atari.)  If no files are specified, or if a file name is "-", the standard input is compressed to the standard output.  Gzip will only attempt to compress regu‐
       lar files.  In particular, it will ignore symbolic links.

       If  the  compressed  file name is too long for its file system, gzip truncates it.  Gzip attempts to truncate only the parts of the file name longer than 3 characters.  (A part is delimited by dots.) If the name consists of
       small parts only, the longest parts are truncated. For example, if file names are limited to 14 characters, gzip.msdos.exe is compressed to gzi.msd.exe.gz.  Names are not truncated on systems which do not have  a  limit  on
       file name length.

       By default, gzip keeps the original file name and timestamp in the compressed file. These are used when decompressing the file with the -N option. This is useful when the compressed file name was truncated or when the time‐
       stamp was not preserved after a file transfer.

       Compressed files can be restored to their original form using gzip -d or gunzip or zcat.  If the original name saved in the compressed file is not suitable for its file system, a new name is constructed  from  the  original
       one to make it legal.

       gunzip takes a list of files on its command line and replaces each file whose name ends with .gz, -gz, .z, -z, or _z (ignoring case) and which begins with the correct magic number with an uncompressed file without the orig‐
       inal extension.  gunzip also recognizes the special extensions .tgz and .taz as shorthands for .tar.gz and .tar.Z respectively.  When compressing, gzip uses the .tgz extension if necessary instead of truncating a file  with
       a .tar extension.

       gunzip  can currently decompress files created by gzip, zip, compress, compress -H or pack.  The detection of the input format is automatic.  When using the first two formats, gunzip checks a 32 bit CRC. For pack and gunzip
       checks the uncompressed length. The standard compress format was not designed to allow consistency checks. However gunzip is sometimes able to detect a bad .Z file. If you get an error when uncompressing a .Z file,  do  not
       assume  that  the  .Z file is correct simply because the standard uncompress does not complain. This generally means that the standard uncompress does not check its input, and happily generates garbage output.  The SCO com‐
       press -H format (lzh compression method) does not include a CRC but also allows some consistency checks.

       Files created by zip can be uncompressed by gzip only if they have a single member compressed with the 'deflation' method. This feature is only intended to help conversion of tar.zip files to the tar.gz format.  To  extract
       a zip file with a single member, use a command like gunzip <foo.zip or gunzip -S .zip foo.zip.  To extract zip files with several members, use unzip instead of gunzip.

       zcat  is  identical  to gunzip -c.  (On some systems, zcat may be installed as gzcat to preserve the original link to compress.)  zcat uncompresses either a list of files on the command line or its standard input and writes
       the uncompressed data on standard output.  zcat will uncompress files that have the correct magic number whether they have a .gz suffix or not.

       Gzip uses the Lempel-Ziv algorithm used in zip and PKZIP.  The amount of compression obtained depends on the size of the input and the distribution of common substrings.  Typically, text such as source code  or  English  is
       reduced by 60-70%.  Compression is generally much better than that achieved by LZW (as used in compress), Huffman coding (as used in pack), or adaptive Huffman coding (compact).

       Compression  is  always  performed,  even if the compressed file is slightly larger than the original. The worst case expansion is a few bytes for the gzip file header, plus 5 bytes every 32K block, or an expansion ratio of
       0.015% for large files. Note that the actual number of used disk blocks almost never increases.  gzip preserves the mode, ownership and timestamps of files when compressing or decompressing.

OPTIONS
       -a --ascii
              Ascii text mode: convert end-of-lines using local conventions. This option is supported only on some non-Unix systems. For MSDOS, CR LF is converted to LF when compressing, and LF is converted to CR  LF  when  decom‐
              pressing.

       -c --stdout --to-stdout
              Write  output on standard output; keep original files unchanged.  If there are several input files, the output consists of a sequence of independently compressed members. To obtain better compression, concatenate all
              input files before compressing them.

       -d --decompress --uncompress
              Decompress.

       -f --force
              Force compression or decompression even if the file has multiple links or the corresponding file already exists, or if the compressed data is read from or written to a terminal. If the input data is not in  a  format
              recognized  by  gzip,  and  if  the  option --stdout is also given, copy the input data without change to the standard output: let zcat behave as cat.  If -f is not given, and when not running in the background, gzip
              prompts to verify whether an existing file should be overwritten.

       -h --help
              Display a help screen and quit.

       -k --keep
              Keep (don't delete) input files during compression or decompression.

       -l --list
              For each compressed file, list the following fields:

                  compressed size: size of the compressed file
                  uncompressed size: size of the uncompressed file
                  ratio: compression ratio (0.0% if unknown)
                  uncompressed_name: name of the uncompressed file

              The uncompressed size is given as -1 for files not in gzip format, such as compressed .Z files. To get the uncompressed size for such a file, you can use:

                  zcat file.Z | wc -c

              In combination with the --verbose option, the following fields are also displayed:

                  method: compression method
                  crc: the 32-bit CRC of the uncompressed data
                  date & time: timestamp for the uncompressed file

              The compression methods currently supported are deflate, compress, lzh (SCO compress -H) and pack.  The crc is given as ffffffff for a file not in gzip format.

              With --name, the uncompressed name,  date and time  are those stored within the compress file if present.

              With --verbose, the size totals and compression ratio for all files is also displayed, unless some sizes are unknown. With --quiet, the title and totals lines are not displayed.

       -L --license
              Display the gzip license and quit.

       -n --no-name
              When compressing, do not save the original file name and timestamp by default. (The original name is always saved if the name had to be truncated.) When decompressing, do not restore the original file name if present
              (remove only the gzip suffix from the compressed file name) and do not restore the original timestamp if present (copy it from the compressed file). This option is the default when decompressing.

       -N --name
              When  compressing,  always  save  the  original file name and timestamp; this is the default. When decompressing, restore the original file name and timestamp if present. This option is useful on systems which have a
              limit on file name length or when the timestamp has been lost after a file transfer.

       -q --quiet
              Suppress all warnings.

       -r --recursive
              Travel the directory structure recursively. If any of the file names specified on the command line are directories, gzip will descend into the directory and compress all the files it finds there (or  decompress  them
              in the case of gunzip ).

       -S .suf --suffix .suf
              When compressing, use suffix .suf instead of .gz.  Any non-empty suffix can be given, but suffixes other than .z and .gz should be avoided to avoid confusion when files are transferred to other systems.

              When decompressing, add .suf to the beginning of the list of suffixes to try, when deriving an output file name from an input file name.

       --synchronous
              Use synchronous output.  With this option, gzip is less likely to lose data during a system crash, but it can be considerably slower.

       -t --test
              Test. Check the compressed file integrity.

       -v --verbose
              Verbose. Display the name and percentage reduction for each file compressed or decompressed.

       -V --version
              Version. Display the version number and compilation options then quit.

       -# --fast --best
              Regulate  the  speed of compression using the specified digit #, where -1 or --fast indicates the fastest compression method (less compression) and -9 or --best indicates the slowest compression method (best compres‐
              sion).  The default compression level is -6 (that is, biased towards high compression at expense of speed).

       --rsyncable
              When you synchronize a compressed file between two computers, this option allows rsync to transfer only files that were changed in the archive instead of the entire archive.  Normally, after a change is made  to  any
              file in the archive, the compression algorithm can generate a new version of the archive that does not match the previous version of the archive. In this case, rsync transfers the entire new version of the archive to
              the remote computer.  With this option, rsync can transfer only the changed files as well as a small amount of metadata that is required to update the archive structure in the area that was changed.

ADVANCED USAGE
       Multiple compressed files can be concatenated. In this case, gunzip will extract all members at once. For example:

             gzip -c file1  > foo.gz
             gzip -c file2 >> foo.gz

       Then

             gunzip -c foo

       is equivalent to

             cat file1 file2

       In case of damage to one member of a .gz file, other members can still be recovered (if the damaged member is removed). However, you can get better compression by compressing all members at once:

             cat file1 file2 | gzip > foo.gz

       compresses better than

             gzip -c file1 file2 > foo.gz

       If you want to recompress concatenated files to get better compression, do:

             gzip -cd old.gz | gzip > new.gz

       If a compressed file consists of several members, the uncompressed size and CRC reported by the --list option applies to the last member only. If you need the uncompressed size for all members, you can use:

             gzip -cd file.gz | wc -c

       If you wish to create a single archive file with multiple members so that members can later be extracted independently, use an archiver such as tar or zip. GNU tar supports the -z option to invoke gzip  transparently.  gzip
       is designed as a complement to tar, not as a replacement.

ENVIRONMENT
       The  obsolescent  environment variable GZIP can hold a set of default options for gzip.  These options are interpreted first and can be overwritten by explicit command line parameters.  As this can cause problems when using
       scripts, this feature is supported only for options that are reasonably likely to not cause too much harm, and gzip warns if it is used.  This feature will be removed in a future release of gzip.

       You can use an alias or script instead.  For example, if gzip is in the directory /usr/bin you can prepend $HOME/bin to your PATH and create an executable script $HOME/bin/gzip containing the following:

             #! /bin/sh
             export PATH=/usr/bin
             exec gzip -9 "$@"

SEE ALSO
       znew(1), zcmp(1), zmore(1), zforce(1), gzexe(1), zip(1), unzip(1), compress(1)

       The gzip file format is specified in P. Deutsch, GZIP file format specification version 4.3, <https://www.ietf.org/rfc/rfc1952.txt>, Internet RFC 1952 (May 1996).  The zip deflation format is specified in  P.  Deutsch,  DE‐
       FLATE Compressed Data Format Specification version 1.3, <https://www.ietf.org/rfc/rfc1951.txt>, Internet RFC 1951 (May 1996).

DIAGNOSTICS
       Exit status is normally 0; if an error occurs, exit status is 1. If a warning occurs, exit status is 2.

       Usage: gzip [-cdfhklLnNrtvV19] [-S suffix] [file ...]
              Invalid options were specified on the command line.

       file: not in gzip format
              The file specified to gunzip has not been compressed.

       file: Corrupt input. Use zcat to recover some data.
              The compressed file has been damaged. The data up to the point of failure can be recovered using

                    zcat file > recover

       file: compressed with xx bits, can only handle yy bits
              File was compressed (using LZW) by a program that could deal with more bits than the decompress code on this machine.  Recompress the file with gzip, which compresses better and uses less memory.

       file: already has .gz suffix -- unchanged
              The file is assumed to be already compressed.  Rename the file and try again.

       file already exists; do you wish to overwrite (y or n)?
              Respond "y" if you want the output file to be replaced; "n" if not.

       gunzip: corrupt input
              A SIGSEGV violation was detected which usually means that the input file has been corrupted.

       xx.x% Percentage of the input saved by compression.
              (Relevant only for -v and -l.)

       -- not a regular file or directory: ignored
              When the input file is not a regular file or directory, (e.g. a symbolic link, socket, FIFO, device file), it is left unaltered.

       -- has xx other links: unchanged
              The input file has links; it is left unchanged.  See ln(1) for more information. Use the -f flag to force compression of multiply-linked files.

CAVEATS
       When  writing  compressed  data to a tape, it is generally necessary to pad the output with zeroes up to a block boundary. When the data is read and the whole block is passed to gunzip for decompression, gunzip detects that
       there is extra trailing garbage after the compressed data and emits a warning by default.  You can use the --quiet option to suppress the warning.

BUGS
       The gzip format represents the input size modulo 2^32, so the --list option reports incorrect uncompressed sizes and compression ratios for uncompressed files 4 GB and larger.  To work around this problem, you can  use  the
       following command to discover a large uncompressed file's true size:

             zcat file.gz | wc -c

       The --list option reports sizes as -1 and crc as ffffffff if the compressed file is on a non seekable media.

       In some rare cases, the --best option gives worse compression than the default compression level (-6). On some highly redundant files, compress compresses better than gzip.

COPYRIGHT NOTICE
       Copyright © 1998-1999, 2001-2002, 2012, 2015-2018 Free Software Foundation, Inc.
       Copyright © 1992, 1993 Jean-loup Gailly

       Permission is granted to make and distribute verbatim copies of this manual provided the copyright notice and this permission notice are preserved on all copies.

       Permission  is granted to copy and distribute modified versions of this manual under the conditions for verbatim copying, provided that the entire resulting derived work is distributed under the terms of a permission notice
       identical to this one.

       Permission is granted to copy and distribute translations of this manual into another language, under the above conditions for modified versions, except that this permission notice may be stated in a translation approved by
       the Foundation.

                                                                                                                 local                                                                                                         GZIP(1)

<a id="zip"></a>
## zip
NAME
       zip - package and compress (archive) files

SYNOPSIS
       zip [-aABcdDeEfFghjklLmoqrRSTuvVwXyz!@$] [--longoption ...]  [-b path] [-n suffixes] [-t date] [-tt date] [zipfile [file ...]]  [-xi list]

       zipcloak (see separate man page)

       zipnote (see separate man page)

       zipsplit (see separate man page)

       Note:  Command line processing in zip has been changed to support long options and handle all options and arguments more consistently.  Some old command lines that depend on command line inconsistencies may no longer work.

DESCRIPTION
       zip  is a compression and file packaging utility for Unix, VMS, MSDOS, OS/2, Windows 9x/NT/XP, Minix, Atari, Macintosh, Amiga, and Acorn RISC OS.  It is analogous to a combination of the Unix commands tar(1) and compress(1)
       and is compatible with PKZIP (Phil Katz's ZIP for MSDOS systems).

       A companion program (unzip(1L)) unpacks zip archives.  The zip and unzip(1L) programs can work with archives produced by PKZIP (supporting most PKZIP features up to PKZIP version 4.6), and PKZIP and PKUNZIP  can  work  with
       archives  produced  by zip (with some exceptions, notably streamed archives, but recent changes in the zip file standard may facilitate better compatibility).  zip version 3.0 is compatible with PKZIP 2.04 and also supports
       the Zip64 extensions of PKZIP 4.5 which allow archives as well as files to exceed the previous 2 GB limit (4 GB in some cases).  zip also now supports bzip2 compression if the bzip2 library is included when zip is compiled.
       Note that PKUNZIP 1.10 cannot extract files produced by PKZIP 2.04 or zip 3.0. You must use PKUNZIP 2.04g or unzip 5.0p1 (or later versions) to extract them.

       See the EXAMPLES section at the bottom of this page for examples of some typical uses of zip.

       Large Archives and Zip64.   zip  automatically  uses the Zip64 extensions when files larger than 4 GB are added to an archive, an archive containing Zip64 entries is updated (if the resulting archive still needs Zip64), the
       size of the archive will exceed 4 GB, or when the number of entries in the archive will exceed about 64K.  Zip64 is also used for archives streamed from standard input as the size of such archives are not known in  advance,
       but the option -fz- can be used to force zip to create PKZIP 2 compatible archives (as long as Zip64 extensions are not needed).  You must use a PKZIP 4.5 compatible unzip, such as unzip 6.0 or later, to extract files using
       the Zip64 extensions.

       In addition, streamed archives, entries encrypted with standard encryption, or split archives created with the pause option may not be compatible with PKZIP as data descriptors are used and PKZIP at the time of this writing
       does not support data descriptors (but recent changes in the PKWare published zip standard now include some support for the data descriptor format zip uses).

       Mac  OS  X.   Though previous Mac versions had their own zip port, zip supports Mac OS X as part of the Unix port and most Unix features apply.  References to "MacOS" below generally refer to MacOS versions older than OS X.
       Support for some Mac OS features in the Unix Mac OS X port, such as resource forks, is expected in the next zip release.

       For a brief help on zip and unzip, run each without specifying any parameters on the command line.

USE
       The program is useful for packaging a set of files for distribution; for archiving files; and for saving disk space by temporarily compressing unused files or directories.

       The zip program puts one or more compressed files into a single zip archive, along with information about the files (name, path, date, time of last modification, protection, and check information to verify file  integrity).
       An entire directory structure can be packed into a zip archive with a single command.  Compression ratios of 2:1 to 3:1 are common for text files.  zip has one compression method (deflation) and can also store files without
       compression.  (If bzip2 support is added, zip can also compress using bzip2 compression, but such entries require a reasonably modern unzip to decompress.  When bzip2 compression is selected, it replaces  deflation  as  the
       default method.)  zip automatically chooses the better of the two (deflation or store or, if bzip2 is selected, bzip2 or store) for each file to be compressed.

       Command format.  The basic command format is

              zip options archive inpath inpath ...

       where  archive  is  a new or existing zip archive and inpath is a directory or file path optionally including wildcards.  When given the name of an existing zip archive, zip will replace identically named entries in the zip
       archive (matching the relative names as stored in the archive) or add entries for new names.  For example, if foo.zip exists and contains foo/file1 and foo/file2, and the directory  foo  contains  the  files  foo/file1  and
       foo/file3, then:

              zip -r foo.zip foo

       or more concisely

              zip -r foo foo

       will replace foo/file1 in foo.zip and add foo/file3 to foo.zip.  After this, foo.zip contains foo/file1, foo/file2, and foo/file3, with foo/file2 unchanged from before.

       So if before the zip command is executed foo.zip has:

               foo/file1 foo/file2

       and directory foo has:

               file1 file3

       then foo.zip will have:

               foo/file1 foo/file2 foo/file3

       where foo/file1 is replaced and foo/file3 is new.

       -@ file lists.  If a file list is specified as -@ [Not on MacOS], zip takes the list of input files from standard input instead of from the command line.  For example,

              zip -@ foo

       will store the files listed one per line on stdin in foo.zip.

       Under Unix, this option can be used to powerful effect in conjunction with the find (1) command.  For example, to archive all the C source files in the current directory and its subdirectories:

              find . -name "*.[ch]" -print | zip source -@

       (note that the pattern must be quoted to keep the shell from expanding it).

       Streaming input and output.  zip will also accept a single dash ("-") as the zip file name, in which case it will write the zip file to standard output, allowing the output to be piped to another program. For example:

              zip -r - . | dd of=/dev/nrst0 obs=16k

       would write the zip output directly to a tape with the specified block size for the purpose of backing up the current directory.

       zip also accepts a single dash ("-") as the name of a file to be compressed, in which case it will read the file from standard input, allowing zip to take input from another program. For example:

              tar cf - . | zip backup -

       would  compress  the  output of the tar command for the purpose of backing up the current directory. This generally produces better compression than the previous example using the -r option because zip can take advantage of
       redundancy between files. The backup can be restored using the command

              unzip -p backup | tar xf -

       When no zip file name is given and stdout is not a terminal, zip acts as a filter, compressing standard input to standard output.  For example,

              tar cf - . | zip | dd of=/dev/nrst0 obs=16k

       is equivalent to

              tar cf - . | zip - - | dd of=/dev/nrst0 obs=16k

       zip archives created in this manner can be extracted with the program funzip which is provided in the unzip package, or by gunzip which is provided in the gzip package (but some gunzip may not support this if zip  used  the
       Zip64 extensions). For example:

              dd if=/dev/nrst0  ibs=16k | funzip | tar xvf -

       The stream can also be saved to a file and unzip used.

       If Zip64 support for large files and archives is enabled and zip is used as a filter, zip creates a Zip64 archive that requires a PKZIP 4.5 or later compatible unzip to read it.  This is to avoid amgibuities in the zip file
       structure as defined in the current zip standard (PKWARE AppNote) where the decision to use Zip64 needs to be made before data is written for the entry, but for a stream the size of the data is not known at that point.   If
       the data is known to be smaller than 4 GB, the option -fz- can be used to prevent use of Zip64, but zip will exit with an error if Zip64 was in fact needed.  zip 3 and unzip 6 and later can read archives with Zip64 entries.
       Also, zip removes the Zip64 extensions if not needed when archive entries are copied (see the -U (--copy) option).

       When directing the output to another file, note that all options should be before the redirection including -x.  For example:

              zip archive "*.h" "*.c" -x donotinclude.h orthis.h > tofile

       Zip files.  When changing an existing zip archive, zip will write a temporary file with the new contents, and only replace the old one when the process of creating the new version has been completed without error.

       If the name of the zip archive does not contain an extension, the extension .zip is added. If the name already contains an extension other than .zip, the existing extension is kept unchanged.  However, split  archives  (ar‐
       chives split over multiple files) require the .zip extension on the last split.

       Scanning and reading files.   When zip starts, it scans for files to process (if needed).  If this scan takes longer than about 5 seconds, zip will display a "Scanning files" message and start displaying progress dots every
       2 seconds or every so many entries processed, whichever takes longer.  If there is more than 2 seconds between dots it could indicate that finding each file is taking time and could mean a slow network connection for  exam‐
       ple.   (Actually  the initial file scan is a two-step process where the directory scan is followed by a sort and these two steps are separated with a space in the dots.  If updating an existing archive, a space also appears
       between the existing file scan and the new file scan.)  The scanning files dots are not controlled by the -ds dot size option, but the dots are turned off by the -q quiet option.  The -sf show files option can  be  used  to
       scan for files and get the list of files scanned without actually processing them.

       If zip is not able to read a file, it issues a warning but continues.  See the -MM option below for more on how zip handles patterns that are not matched and files that are not readable.  If some files were skipped, a warn‐
       ing is issued at the end of the zip operation noting how many files were read and how many skipped.

       Command modes.  zip now supports two distinct types of command modes, external and internal.  The external modes (add, update, and freshen) read files from the file system (as well as from an existing archive) while the in‐
       ternal modes (delete and copy) operate exclusively on entries in an existing archive.

       add
              Update existing entries and add new files.  If the archive does not exist create it.  This is the default mode.

       update (-u)
              Update existing entries if newer on the file system and add new files.  If the archive does not exist issue warning then create a new archive.

       freshen (-f)
              Update existing entries of an archive if newer on the file system.  Does not add new files to the archive.

       delete (-d)
              Select entries in an existing archive and delete them.

       copy (-U)
              Select entries in an existing archive and copy them to a new archive.  This new mode is similar to update but command line patterns select entries in the existing archive rather than files from the file system and it
              uses the --out option to write the resulting archive to a new file rather than update the existing archive, leaving the original archive unchanged.

       The new File Sync option (-FS) is also considered a new mode, though it is similar to update.  This mode synchronizes the archive with the files on the OS, only replacing files in the archive if the file time or size of the
       OS file is different, adding new files, and deleting entries from the archive where there is no matching file.  As this mode can delete entries from the archive, consider making a backup copy of the archive.

       Also see -DF for creating difference archives.

       See each option description below for details and the EXAMPLES section below for examples.

       Split archives.  zip version 3.0 and later can create split archives.  A split archive is a standard zip archive split over multiple files.  (Note that split archives are not just archives split in to pieces, as the offsets
       of entries are now based on the start of each split.  Concatenating the pieces together will invalidate these offsets, but unzip can usually deal with it.  zip will usually refuse to process such a  spliced  archive  unless
       the -FF fix option is used to fix the offsets.)

       One  use  of  split  archives  is  storing a large archive on multiple removable media.  For a split archive with 20 split files the files are typically named (replace ARCHIVE with the name of your archive) ARCHIVE.z01, AR‐
       CHIVE.z02, ..., ARCHIVE.z19, ARCHIVE.zip.  Note that the last file is the .zip file.  In contrast, spanned archives are the original multi-disk archive generally requiring floppy disks and using volume labels to store  disk
       numbers.   zip supports split archives but not spanned archives, though a procedure exists for converting split archives of the right size to spanned archives.  The reverse is also true, where each file of a spanned archive
       can be copied in order to files with the above names to create a split archive.

       Use -s to set the split size and create a split archive.  The size is given as a number followed optionally by one of k (kB), m (MB), g (GB), or t (TB) (the default is m).  The -sp option can be used to  pause  zip  between
       splits to allow changing removable media, for example, but read the descriptions and warnings for both -s and -sp below.

       Though zip does not update split archives, zip provides the new option -O (--output-file or --out) to allow split archives to be updated and saved in a new archive.  For example,

              zip inarchive.zip foo.c bar.c --out outarchive.zip

       reads  archive inarchive.zip, even if split, adds the files foo.c and bar.c, and writes the resulting archive to outarchive.zip.  If inarchive.zip is split then outarchive.zip defaults to the same split size.  Be aware that
       if outarchive.zip and any split files that are created with it already exist, these are always overwritten as needed without warning.  This may be changed in the future.

       Unicode.  Though the zip standard requires storing paths in an archive using a specific character set, in practice zips have stored paths in archives in whatever the local character set is.  This creates  problems  when  an
       archive  is created or updated on a system using one character set and then extracted on another system using a different character set.  When compiled with Unicode support enabled on platforms that support wide characters,
       zip now stores, in addition to the standard local path for backward compatibility, the UTF-8 translation of the path.  This provides a common universal character set for storing paths that allows these paths to be fully ex‐
       tracted on other systems that support Unicode and to match as close as possible on systems that don't.

       On  Win32 systems where paths are internally stored as Unicode but represented in the local character set, it's possible that some paths will be skipped during a local character set directory scan.  zip with Unicode support
       now can read and store these paths.  Note that Win 9x systems and FAT file systems don't fully support Unicode.

       Be aware that console windows on Win32 and Unix, for example, sometimes don't accurately show all characters due to how each operating system switches in character sets for  display.   However,  directory  navigation  tools
       should show the correct paths if the needed fonts are loaded.

       Command line format.  This version of zip has updated command line processing and support for long options.

       Short options take the form

              -s[-][s[-]...][value][=value][ value]

       where  s  is  a one or two character short option.  A short option that takes a value is last in an argument and anything after it is taken as the value.  If the option can be negated and "-" immediately follows the option,
       the option is negated.  Short options can also be given as separate arguments

              -s[-][value][=value][ value] -s[-][value][=value][ value] ...

       Short options in general take values either as part of the same argument or as the following argument.  An optional = is also supported.  So

              -ttmmddyyyy

       and

              -tt=mmddyyyy

       and

              -tt mmddyyyy

       all work.  The -x and -i options accept lists of values and use a slightly different format described below.  See the -x and -i options.

       Long options take the form

              --longoption[-][=value][ value]

       where the option starts with --, has a multicharacter name, can include a trailing dash to negate the option (if the option supports it), and can have a value (option argument) specified by preceeding it with = (no spaces).
       Values can also follow the argument.  So

              --before-date=mmddyyyy

       and

              --before-date mmddyyyy

       both work.

       Long  option  names  can  be shortened to the shortest unique abbreviation.  See the option descriptions below for which support long options.  To avoid confusion, avoid abbreviating a negatable option with an embedded dash
       ("-") at the dash if you plan to negate it (the parser would consider a trailing dash, such as for the option --some-option using --some- as the option, as part of the name rather than a negating dash).  This may be changed
       to force the last dash in --some- to be negating in the future.

OPTIONS
       -a
       --ascii
              [Systems using EBCDIC] Translate file to ASCII format.

       -A
       --adjust-sfx
              Adjust self-extracting executable archive.  A self-extracting executable archive is created by prepending the SFX stub to an existing archive. The -A option tells zip to adjust the entry offsets stored in the archive
              to take into account this "preamble" data.

       Note: self-extracting archives for the Amiga are a special case.  At present, only the Amiga port of zip is capable of adjusting or updating these without corrupting them. -J can be used to remove the SFX stub if other  up‐
       dates need to be made.

       -AC
       --archive-clear
              [WIN32]   Once  archive  is created (and tested if -T is used, which is recommended), clear the archive bits of files processed.  WARNING: Once the bits are cleared they are cleared.  You may want to use the -sf show
              files option to store the list of files processed in case the archive operation must be repeated.  Also consider using the -MM must match option.  Be sure to check out -DF as a possibly better way to  do  incremental
              backups.

       -AS
       --archive-set
              [WIN32]   Only include files that have the archive bit set.  Directories are not stored when -AS is used, though by default the paths of entries, including directories, are stored as usual and can be used by most un‐
              zips to recreate directories.

              The archive bit is set by the operating system when a file is modified and, if used with -AC, -AS can provide an incremental backup capability.  However, other applications can modify the archive bit and it  may  not
              be a reliable indicator of which files have changed since the last archive operation.  Alternative ways to create incremental backups are using -t to use file dates, though this won't catch old files copied to direc‐
              tories being archived, and -DF to create a differential archive.

       -B
       --binary
              [VM/CMS and MVS] force file to be read binary (default is text).

       -Bn    [TANDEM] set Edit/Enscribe formatting options with n defined as
              bit  0: Don't add delimiter (Edit/Enscribe)
              bit  1: Use LF rather than CR/LF as delimiter (Edit/Enscribe)
              bit  2: Space fill record to maximum record length (Enscribe)
              bit  3: Trim trailing space (Enscribe)
              bit  8: Force 30K (Expand) large read for unstructured files

       -b path
       --temp-path path
              Use the specified path for the temporary zip archive. For example:

                     zip -b /tmp stuff *

              will put the temporary zip archive in the directory /tmp, copying over stuff.zip to the current directory when done. This option is useful when updating an existing archive and the file system containing this old ar‐
              chive  does  not  have enough space to hold both old and new archives at the same time.  It may also be useful when streaming in some cases to avoid the need for data descriptors.  Note that using this option may re‐
              quire zip take additional time to copy the archive file when done to the destination file system.

       -c
       --entry-comments
              Add one-line comments for each file.  File operations (adding, updating) are done first, and the user is then prompted for a one-line comment for each file.  Enter the comment followed by return, or just  return  for
              no comment.

       -C
       --preserve-case
              [VMS]  Preserve case all on VMS.  Negating this option (-C-) downcases.

       -C2
       --preserve-case-2
              [VMS]  Preserve case ODS2 on VMS.  Negating this option (-C2-) downcases.

       -C5
       --preserve-case-5
              [VMS]  Preserve case ODS5 on VMS.  Negating this option (-C5-) downcases.

       -d
       --delete
              Remove (delete) entries from a zip archive.  For example:

                     zip -d foo foo/tom/junk foo/harry/\* \*.o

              will  remove  the entry foo/tom/junk, all of the files that start with foo/harry/, and all of the files that end with .o (in any path).  Note that shell pathname expansion has been inhibited with backslashes, so that
              zip can see the asterisks, enabling zip to match on the contents of the zip archive instead of the contents of the current directory.  (The backslashes are not used on MSDOS-based platforms.)  Can also use quotes  to
              escape the asterisks as in

                     zip -d foo foo/tom/junk "foo/harry/*" "*.o"

              Not  escaping  the  asterisks  on a system where the shell expands wildcards could result in the asterisks being converted to a list of files in the current directory and that list used to delete entries from the ar‐
              chive.

              Under MSDOS, -d is case sensitive when it matches names in the zip archive.  This requires that file names be entered in upper case if they were zipped by PKZIP on an MSDOS system.  (We considered  making  this  case
              insensitive  on  systems  where  paths were case insensitive, but it is possible the archive came from a system where case does matter and the archive could include both Bar and bar as separate files in the archive.)
              But see the new option -ic to ignore case in the archive.

       -db
       --display-bytes
              Display running byte counts showing the bytes zipped and the bytes to go.

       -dc
       --display-counts
              Display running count of entries zipped and entries to go.

       -dd
       --display-dots
              Display dots while each entry is zipped (except on ports that have their own progress indicator).  See -ds below for setting dot size.  The default is a dot every 10 MB of input file processed.  The  -v  option  also
              displays dots (previously at a much higher rate than this but now -v also defaults to 10 MB) and this rate is also controlled by -ds.

       -df
       --datafork
              [MacOS] Include only data-fork of files zipped into the archive.  Good for exporting files to foreign operating-systems.  Resource-forks will be ignored at all.

       -dg
       --display-globaldots
              Display progress dots for the archive instead of for each file.  The command

                         zip -qdgds 10m

              will turn off most output except dots every 10 MB.

       -ds size
       --dot-size size
              Set  amount  of input file processed for each dot displayed.  See -dd to enable displaying dots.  Setting this option implies -dd.  Size is in the format nm where n is a number and m is a multiplier.  Currently m can
              be k (KB), m (MB), g (GB), or t (TB), so if n is 100 and m is k, size would be 100k which is 100 KB.  The default is 10 MB.

              The -v option also displays dots and now defaults to 10 MB also.  This rate is also controlled by this option.  A size of 0 turns dots off.

              This option does not control the dots from the "Scanning files" message as zip scans for input files.  The dot size for that is fixed at 2 seconds or a fixed number of entries, whichever is longer.

       -du
       --display-usize
              Display the uncompressed size of each entry.

       -dv
       --display-volume
              Display the volume (disk) number each entry is being read from, if reading an existing archive, and being written to.

       -D
       --no-dir-entries
              Do not create entries in the zip archive for directories.  Directory entries are created by default so that their attributes can be saved in the zip archive.  The environment variable ZIPOPT can be used to change the
              default options. For example under Unix with sh:

                     ZIPOPT="-D"; export ZIPOPT

              (The  variable  ZIPOPT  can  be  used for any option, including -i and -x using a new option format detailed below, and can include several options.) The option -D is a shorthand for -x "*/" but the latter previously
              could not be set as default in the ZIPOPT environment variable as the contents of ZIPOPT gets inserted near the beginning of the command line and the file list had to end at the end of the line.

              This version of zip does allow -x and -i options in ZIPOPT if the form

               -x file file ... @

              is used, where the @ (an argument that is just @) terminates the list.

       -DF
       --difference-archive
              Create an archive that contains all new and changed files since the original archive was created.  For this to work, the input file list and current directory must be the same as during the original zip operation.

              For example, if the existing archive was created using

                     zip -r foofull .

              from the bar directory, then the command

                     zip -r foofull . -DF --out foonew

              also from the bar directory creates the archive foonew with just the files not in foofull and the files where the size or file time of the files do not match those in foofull.

              Note that the timezone environment variable TZ should be set according to the local timezone in order for this option to work correctly.  A change in timezone since the original archive was created could result in no
              times matching and all files being included.

              A possible approach to backing up a directory might be to create a normal archive of the contents of the directory as a full backup, then use this option to create incremental backups.

       -e
       --encrypt
              Encrypt  the contents of the zip archive using a password which is entered on the terminal in response to a prompt (this will not be echoed; if standard error is not a tty, zip will exit with an error).  The password
              prompt is repeated to save the user from typing errors.

       -E
       --longnames
              [OS/2] Use the .LONGNAME Extended Attribute (if found) as filename.

       -f
       --freshen
              Replace (freshen) an existing entry in the zip archive only if it has been modified more recently than the version already in the zip archive; unlike the update option (-u) this will not add files that  are  not  al‐
              ready in the zip archive.  For example:

                     zip -f foo

              This command should be run from the same directory from which the original zip command was run, since paths stored in zip archives are always relative.

              Note that the timezone environment variable TZ should be set according to the local timezone in order for the -f, -u and -o options to work correctly.

              The reasons behind this are somewhat subtle but have to do with the differences between the Unix-format file times (always in GMT) and most of the other operating systems (always local time) and the necessity to com‐
              pare the two.  A typical TZ value is ``MET-1MEST'' (Middle European time with automatic adjustment for ``summertime'' or Daylight Savings Time).

              The format is TTThhDDD, where TTT is the time zone such as MET, hh is the difference between GMT and local time such as -1 above, and DDD is the time zone when daylight savings time is in effect.  Leave off  the  DDD
              if there is no daylight savings time.  For the US Eastern time zone EST5EDT.

       -F
       --fix
       -FF
       --fixfix
              Fix  the  zip archive. The -F option can be used if some portions of the archive are missing, but requires a reasonably intact central directory.  The input archive is scanned as usual, but zip will ignore some prob‐
              lems.  The resulting archive should be valid, but any inconsistent entries will be left out.

              When doubled as in -FF, the archive is scanned from the beginning and zip scans for special signatures to identify the limits between the archive members. The single -F is more reliable if the archive is not too much
              damaged, so try this option first.

              If the archive is too damaged or the end has been truncated, you must use -FF.  This is a change from zip 2.32, where the -F option is able to read a truncated archive.  The -F option now more reliably fixes archives
              with minor damage and the -FF option is needed to fix archives where -F might have been sufficient before.

              Neither option will recover archives that have been incorrectly transferred in ascii mode instead of binary. After the repair, the -t option of unzip may show that some files have a bad CRC. Such files cannot be  re‐
              covered; you can remove them from the archive using the -d option of zip.

              Note  that  -FF may have trouble fixing archives that include an embedded zip archive that was stored (without compression) in the archive and, depending on the damage, it may find the entries in the embedded archive
              rather than the archive itself.  Try -F first as it does not have this problem.

              The format of the fix commands have changed.  For example, to fix the damaged archive foo.zip,

                     zip -F foo --out foofix

              tries to read the entries normally, copying good entries to the new archive foofix.zip.  If this doesn't work, as when the archive is truncated, or if some entries you know are in the archive are missed, then try

                     zip -FF foo --out foofixfix

              and compare the resulting archive to the archive created by -F.  The -FF option may create an inconsistent archive.  Depending on what is damaged, you can then use the -F option to fix that archive.

              A split archive with missing split files can be fixed using -F if you have the last split of the archive (the .zip file).  If this file is missing, you must use -FF to fix the archive, which will prompt you  for  the
              splits you have.

              Currently the fix options can't recover entries that have a bad checksum or are otherwise damaged.

       -FI
       --fifo [Unix]  Normally zip skips reading any FIFOs (named pipes) encountered, as zip can hang if the FIFO is not being fed.  This option tells zip to read the contents of any FIFO it finds.

       -FS
       --filesync
              Synchronize  the  contents of an archive with the files on the OS.  Normally when an archive is updated, new files are added and changed files are updated but files that no longer exist on the OS are not deleted from
              the archive.  This option enables a new mode that checks entries in the archive against the file system.  If the file time and file size of the entry matches that of the OS file, the entry is copied from the old  ar‐
              chive  instead  of  being  read  from the file system and compressed.  If the OS file has changed, the entry is read and compressed as usual.  If the entry in the archive does not match a file on the OS, the entry is
              deleted.  Enabling this option should create archives that are the same as new archives, but since existing entries are copied instead of compressed, updating an existing archive with -FS can be much faster than cre‐
              ating a new archive.  Also consider using -u for updating an archive.

              For  this option to work, the archive should be updated from the same directory it was created in so the relative paths match.  If few files are being copied from the old archive, it may be faster to create a new ar‐
              chive instead.

              Note that the timezone environment variable TZ should be set according to the local timezone in order for this option to work correctly.  A change in timezone since the original archive was created could result in no
              times matching and recompression of all files.

              This  option deletes files from the archive.  If you need to preserve the original archive, make a copy of the archive first or use the --out option to output the updated archive to a new file.  Even though it may be
              slower, creating a new archive with a new archive name is safer, avoids mismatches between archive and OS paths, and is preferred.

       -g
       --grow
              Grow (append to) the specified zip archive, instead of creating a new one. If this operation fails, zip attempts to restore the archive to its original state. If the restoration fails, the archive might  become  cor‐
              rupted. This option is ignored when there's no existing archive or when at least one archive member must be updated or deleted.

       -h
       -?
       --help
              Display the zip help information (this also appears if zip is run with no arguments).

       -h2
       --more-help
              Display extended help including more on command line format, pattern matching, and more obscure options.

       -i files
       --include files
              Include only the specified files, as in:

                     zip -r foo . -i \*.c

              which will include only the files that end in .c in the current directory and its subdirectories. (Note for PKZIP users: the equivalent command is

                     pkzip -rP foo *.c

              PKZIP  does  not allow recursion in directories other than the current one.)  The backslash avoids the shell filename substitution, so that the name matching is performed by zip at all directory levels.  [This is for
              Unix and other systems where \  escapes the next character.  For other systems where the shell does not process * do not use \ and the above is

                     zip -r foo . -i *.c

              Examples are for Unix unless otherwise specified.]  So to include dir, a directory directly under the current directory, use

                     zip -r foo . -i dir/\*

              or

                     zip -r foo . -i "dir/*"

              to match paths such as dir/a and dir/b/file.c [on ports without wildcard expansion in the shell such as MSDOS and Windows

                     zip -r foo . -i dir/*

              is used.]  Note that currently the trailing / is needed for directories (as in

                     zip -r foo . -i dir/

              to include directory dir).

              The long option form of the first example is

                     zip -r foo . --include \*.c

              and does the same thing as the short option form.

              Though the command syntax used to require -i at the end of the command line, this version actually allows -i (or --include) anywhere.  The list of files terminates at the next argument starting with -, the end of the
              command line, or the list terminator @ (an argument that is just @).  So the above can be given as

                     zip -i \*.c @ -r foo .

              for example.  There must be a space between the option and the first file of a list.  For just one file you can use the single value form

                     zip -i\*.c -r foo .

              (no space between option and value) or

                     zip --include=\*.c -r foo .

              as  additional  examples.   The single value forms are not recommended because they can be confusing and, in particular, the -ifile format can cause problems if the first letter of file combines with i to form a two-
              letter option starting with i.  Use -sc to see how your command line will be parsed.

              Also possible:

                     zip -r foo  . -i@include.lst

              which will only include the files in the current directory and its subdirectories that match the patterns in the file include.lst.

              Files to -i and -x are patterns matching internal archive paths.  See -R for more on patterns.

       -I
       --no-image
              [Acorn RISC OS] Don't scan through Image files.  When used, zip will not consider Image files (eg. DOS partitions or Spark archives when SparkFS is loaded) as directories but will store them as single files.

              For example, if you have SparkFS loaded, zipping a Spark archive will result in a zipfile containing a directory (and its content) while using the 'I' option will result in a zipfile containing a Spark archive. Obvi‐
              ously this second case will also be obtained (without the 'I' option) if SparkFS isn't loaded.

       -ic
       --ignore-case
              [VMS,  WIN32]  Ignore  case  when  matching archive entries.  This option is only available on systems where the case of files is ignored.  On systems with case-insensitive file systems, case is normally ignored when
              matching files on the file system but is not ignored for -f (freshen), -d (delete), -U (copy), and similar modes when matching against archive entries (currently -f ignores case on VMS) because archive entries can be
              from  systems  where  case does matter and names that are the same except for case can exist in an archive.  The -ic option makes all matching case insensitive.  This can result in multiple archive entries matching a
              command line pattern.

       -j
       --junk-paths
              Store just the name of a saved file (junk the path), and do not store directory names. By default, zip will store the full path (relative to the current directory).

       -jj
       --absolute-path
              [MacOS] record Fullpath (+ Volname). The complete path including volume will be stored. By default the relative path will be stored.

       -J
       --junk-sfx
              Strip any prepended data (e.g. a SFX stub) from the archive.

       -k
       --DOS-names
              Attempt to convert the names and paths to conform to MSDOS, store only the MSDOS attribute (just the user write attribute from Unix), and mark the entry as made under MSDOS (even though it was not); for compatibility
              with PKUNZIP under MSDOS which cannot handle certain names such as those with two dots.

       -l
       --to-crlf
              Translate  the  Unix  end-of-line character LF into the MSDOS convention CR LF. This option should not be used on binary files.  This option can be used on Unix if the zip file is intended for PKUNZIP under MSDOS. If
              the input files already contain CR LF, this option adds an extra CR. This is to ensure that unzip -a on Unix will get back an exact copy of the original file, to undo the effect of zip -l.  See  -ll  for  how  binary
              files are handled.

       -la
       --log-append
              Append to existing logfile.  Default is to overwrite.

       -lf logfilepath
       --logfile-path logfilepath
              Open  a  logfile  at the given path.  By default any existing file at that location is overwritten, but the -la option will result in an existing file being opened and the new log information appended to any existing
              information.  Only warnings and errors are written to the log unless the -li option is also given, then all information messages are also written to the log.

       -li
       --log-info
              Include information messages, such as file names being zipped, in the log.  The default is to only include the command line, any warnings and errors, and the final status.

       -ll
       --from-crlf
              Translate the MSDOS end-of-line CR LF into Unix LF.  This option should not be used on binary files.  This option can be used on MSDOS if the zip file is intended for unzip under Unix.  If the file is  converted  and
              the  file  is later determined to be binary a warning is issued and the file is probably corrupted.  In this release if -ll detects binary in the first buffer read from a file, zip now issues a warning and skips line
              end conversion on the file.  This check seems to catch all binary files tested, but the original check remains and if a converted file is later determined to be binary that warning is still issued.  A  new  algorithm
              is now being used for binary detection that should allow line end conversion of text files in UTF-8 and similar encodings.

       -L
       --license
              Display the zip license.

       -m
       --move
              Move  the  specified  files  into the zip archive; actually, this deletes the target directories/files after making the specified zip archive. If a directory becomes empty after removal of the files, the directory is
              also removed. No deletions are done until zip has created the archive without error.  This is useful for conserving disk space, but is potentially dangerous so it is recommended to use it in combination  with  -T  to
              test the archive before removing all input files.

       -MM
       --must-match
              All  input  patterns  must match at least one file and all input files found must be readable.  Normally when an input pattern does not match a file the "name not matched" warning is issued and when an input file has
              been found but later is missing or not readable a missing or not readable warning is issued.  In either case zip continues creating the archive, with missing or unreadable new files being skipped and files already in
              the  archive remaining unchanged.  After the archive is created, if any files were not readable zip returns the OPEN error code (18 on most systems) instead of the normal success return (0 on most systems).  With -MM
              set, zip exits as soon as an input pattern is not matched (whenever the "name not matched" warning would be issued) or when an input file is not readable.  In either case zip exits with an OPEN error and  no  archive
              is created.

              This  option  is useful when a known list of files is to be zipped so any missing or unreadable files will result in an error.  It is less useful when used with wildcards, but zip will still exit with an error if any
              input pattern doesn't match at least one file and if any matched files are unreadable.  If you want to create the archive anyway and only need to know if files were skipped, don't use -MM and just  check  the  return
              code.  Also -lf could be useful.

       -n suffixes
       --suffixes suffixes
              Do  not  attempt  to  compress files named with the given suffixes.  Such files are simply stored (0% compression) in the output zip file, so that zip doesn't waste its time trying to compress them.  The suffixes are
              separated by either colons or semicolons.  For example:

                     zip -rn .Z:.zip:.tiff:.gif:.snd  foo foo

              will copy everything from foo into foo.zip, but will store any files that end in .Z, .zip, .tiff, .gif, or .snd without trying to compress them (image and sound files often  have  their  own  specialized  compression
              methods).   By  default,  zip  does  not  compress files with extensions in the list .Z:.zip:.zoo:.arc:.lzh:.arj.  Such files are stored directly in the output archive.  The environment variable ZIPOPT can be used to
              change the default options. For example under Unix with csh:

                     setenv ZIPOPT "-n .gif:.zip"

              To attempt compression on all files, use:

                     zip -n : foo

              The maximum compression option -9 also attempts compression on all files regardless of extension.

              On Acorn RISC OS systems the suffixes are actually filetypes (3 hex digit format). By default, zip does not compress files with filetypes in the list DDC:D96:68E (i.e. Archives, CFS files and PackDir files).

       -nw
       --no-wild
              Do not perform internal wildcard processing (shell processing of wildcards is still done by the shell unless the arguments are escaped).  Useful if a list of paths is being read and no wildcard  substitution  is  de‐
              sired.

       -N
       --notes
              [Amiga,  MacOS]  Save  Amiga  or  MacOS  filenotes  as  zipfile  comments. They can be restored by using the -N option of unzip. If -c is used also, you are prompted for comments only for those files that do not have
              filenotes.

       -o
       --latest-time
              Set the "last modified" time of the zip archive to the latest (oldest) "last modified" time found among the entries in the zip archive.  This can be used without any other operations, if desired.  For example:

              zip -o foo

              will change the last modified time of foo.zip to the latest time of the entries in foo.zip.

       -O output-file
       --output-file output-file
              Process the archive changes as usual, but instead of updating the existing archive, output the new archive to output-file.  Useful for updating an archive without changing the existing archive and the  input  archive
              must be a different file than the output archive.

              This option can be used to create updated split archives.  It can also be used with -U to copy entries from an existing archive to a new archive.  See the EXAMPLES section below.

              Another use is converting zip files from one split size to another.  For instance, to convert an archive with 700 MB CD splits to one with 2 GB DVD splits, can use:

                     zip -s 2g cd-split.zip --out dvd-split.zip

              which uses copy mode.  See -U below.  Also:

                     zip -s 0 split.zip --out unsplit.zip

              will convert a split archive to a single-file archive.

              Copy  mode  will convert stream entries (using data descriptors and which should be compatible with most unzips) to normal entries (which should be compatible with all unzips), except if standard encryption was used.
              For archives with encrypted entries, zipcloak will decrypt the entries and convert them to normal entries.

       -p
       --paths
              Include relative file paths as part of the names of files stored in the archive.  This is the default.  The -j option junks the paths and just stores the names of the files.

       -P password
       --password password
              Use password to encrypt zipfile entries (if any).  THIS IS INSECURE!  Many multi-user operating systems provide ways for any user to see the current command line of any other user; even on stand-alone  systems  there
              is  always the threat of over-the-shoulder peeking.  Storing the plaintext password as part of a command line in an automated script is even worse.  Whenever possible, use the non-echoing, interactive prompt to enter
              passwords.  (And where security is truly important, use strong encryption such as Pretty Good Privacy instead of the relatively weak standard encryption provided by zipfile utilities.)

       -q
       --quiet
              Quiet mode; eliminate informational messages and comment prompts.  (Useful, for example, in shell scripts and background tasks).

       -Qn
       --Q-flag n
              [QDOS] store information about the file in the file header with n defined as
              bit  0: Don't add headers for any file
              bit  1: Add headers for all files
              bit  2: Don't wait for interactive key press on exit

       -r
       --recurse-paths
              Travel the directory structure recursively; for example:

                     zip -r foo.zip foo

              or more concisely

                     zip -r foo foo

              In this case, all the files and directories in foo are saved in a zip archive named foo.zip, including files with names starting with ".", since the recursion does not use the shell's  file-name  substitution  mecha‐
              nism.   If you wish to include only a specific subset of the files in directory foo and its subdirectories, use the -i option to specify the pattern of files to be included.  You should not use -r with the name ".*",
              since that matches ".."  which will attempt to zip up the parent directory (probably not what was intended).

              Multiple source directories are allowed as in

                     zip -r foo foo1 foo2

              which first zips up foo1 and then foo2, going down each directory.

              Note that while wildcards to -r are typically resolved while recursing down directories in the file system, any -R, -x, and -i wildcards are applied to internal archive pathnames once the directories are scanned.  To
              have  wildcards apply to files in subdirectories when recursing on Unix and similar systems where the shell does wildcard substitution, either escape all wildcards or put all arguments with wildcards in quotes.  This
              lets zip see the wildcards and match files in subdirectories using them as it recurses.

       -R
       --recurse-patterns
              Travel the directory structure recursively starting at the current directory; for example:

                     zip -R foo "*.c"

              In this case, all the files matching *.c in the tree starting at the current directory are stored into a zip archive named foo.zip.  Note that *.c will match file.c, a/file.c and a/b/.c.  More than one pattern can be
              listed as separate arguments.  Note for PKZIP users: the equivalent command is

                     pkzip -rP foo *.c

              Patterns  are  relative file paths as they appear in the archive, or will after zipping, and can have optional wildcards in them.  For example, given the current directory is foo and under it are directories foo1 and
              foo2 and in foo1 is the file bar.c,

                     zip -R foo/*

              will zip up foo, foo/foo1, foo/foo1/bar.c, and foo/foo2.

                     zip -R */bar.c

              will zip up foo/foo1/bar.c.  See the note for -r on escaping wildcards.

       -RE
       --regex
              [WIN32]  Before zip 3.0, regular expression list matching was enabled by default on Windows platforms.  Because of confusion resulting from the need to escape "[" and "]" in names, it is now off by default  for  Win‐
              dows so "[" and "]" are just normal characters in names.  This option enables [] matching again.

       -s splitsize
       --split-size splitsize
              Enable  creating  a  split  archive and set the split size.  A split archive is an archive that could be split over many files.  As the archive is created, if the size of the archive reaches the specified split size,
              that split is closed and the next split opened.  In general all splits but the last will be the split size and the last will be whatever is left.  If the entire archive is smaller than the split  size  a  single-file
              archive is created.

              Split  archives  are  stored  in  numbered files.  For example, if the output archive is named archive and three splits are required, the resulting archive will be in the three files archive.z01, archive.z02, and ar‐
              chive.zip.  Do not change the numbering of these files or the archive will not be readable as these are used to determine the order the splits are read.

              Split size is a number optionally followed by a multiplier.  Currently the number must be an integer.  The multiplier can currently be one of k (kilobytes), m (megabytes), g (gigabytes), or t (terabytes).  As 64k  is
              the minimum split size, numbers without multipliers default to megabytes.  For example, to create a split archive called foo with the contents of the bar directory with splits of 670 MB that might be useful for burn‐
              ing on CDs, the command:

                     zip -s 670m -r foo bar

              could be used.

              Currently the old splits of a split archive are not excluded from a new archive, but they can be specifically excluded.  If possible, keep the input and output archives out of the  path  being  zipped  when  creating
              split archives.

              Using -s without -sp as above creates all the splits where foo is being written, in this case the current directory.  This split mode updates the splits as the archive is being created, requiring all splits to remain
              writable, but creates split archives that are readable by any unzip that supports split archives.  See -sp below for enabling split pause mode which allows splits to be written directly to removable media.

              The option -sv can be used to enable verbose splitting and provide details of how the splitting is being done.  The -sb option can be used to ring the bell when zip pauses for the next split destination.

              Split archives cannot be updated, but see the -O (--out) option for how a split archive can be updated as it is copied to a new archive.  A split archive can also be converted into a single-file archive using a split
              size of 0 or negating the -s option:

                     zip -s 0 split.zip --out single.zip

              Also see -U (--copy) for more on using copy mode.

       -sb
       --split-bell
              If splitting and using split pause mode, ring the bell when zip pauses for each split destination.

       -sc
       --show-command
              Show  the  command line starting zip as processed and exit.  The new command parser permutes the arguments, putting all options and any values associated with them before any non-option arguments.  This allows an op‐
              tion to appear anywhere in the command line as long as any values that go with the option go with it.  This option displays the command line as zip sees it, including any arguments from the environment such  as  from
              the ZIPOPT variable.  Where allowed, options later in the command line can override options earlier in the command line.

       -sf
       --show-files
              Show  the  files that would be operated on, then exit.  For instance, if creating a new archive, this will list the files that would be added.  If the option is negated, -sf-, output only to an open log file.  Screen
              display is not recommended for large lists.

       -so
       --show-options
              Show all available options supported by zip as compiled on the current system.  As this command reads the option table, it should include all options.  Each line includes the short option (if defined), the  long  op‐
              tion  (if defined), the format of any value that goes with the option, if the option can be negated, and a small description.  The value format can be no value, required value, optional value, single character value,
              number value, or a list of values.  The output of this option is not intended to show how to use any option but only show what options are available.

       -sp
       --split-pause
              If splitting is enabled with -s, enable split pause mode.  This creates split archives as -s does, but stream writing is used so each split can be closed as soon as it is written and zip will pause between each split
              to allow changing split destination or media.

              Though  this  split mode allows writing splits directly to removable media, it uses stream archive format that may not be readable by some unzips.  Before relying on splits created with -sp, test a split archive with
              the unzip you will be using.

              To convert a stream split archive (created with -sp) to a standard archive see the --out option.

       -su
       --show-unicode
              As -sf, but also show Unicode version of the path if exists.

       -sU
       --show-just-unicode
              As -sf, but only show Unicode version of the path if exists, otherwise show the standard version of the path.

       -sv
       --split-verbose
              Enable various verbose messages while splitting, showing how the splitting is being done.

       -S
       --system-hidden
              [MSDOS, OS/2, WIN32 and ATARI] Include system and hidden files.
              [MacOS] Includes finder invisible files, which are ignored otherwise.

       -t mmddyyyy
       --from-date mmddyyyy
              Do not operate on files modified prior to the specified date, where mm is the month (00-12), dd is the day of the month (01-31), and yyyy is the year.  The ISO 8601 date format yyyy-mm-dd is also accepted.  For exam‐
              ple:

                     zip -rt 12071991 infamy foo

                     zip -rt 1991-12-07 infamy foo

              will add all the files in foo and its subdirectories that were last modified on or after 7 December 1991, to the zip archive infamy.zip.

       -tt mmddyyyy
       --before-date mmddyyyy
              Do  not  operate  on files modified after or at the specified date, where mm is the month (00-12), dd is the day of the month (01-31), and yyyy is the year.  The ISO 8601 date format yyyy-mm-dd is also accepted.  For
              example:

                     zip -rtt 11301995 infamy foo

                     zip -rtt 1995-11-30 infamy foo

              will add all the files in foo and its subdirectories that were last modified before 30 November 1995, to the zip archive infamy.zip.

       -T
       --test
              Test the integrity of the new zip file. If the check fails, the old zip file is unchanged and (with the -m option) no input files are removed.

       -TT cmd
       --unzip-command cmd
              Use command cmd instead of 'unzip -tqq' to test an archive when the -T option is used.  On Unix, to use a copy of unzip in the current directory instead of the standard system unzip, could use:

               zip archive file1 file2 -T -TT "./unzip -tqq"

              In cmd, {} is replaced by the name of the temporary archive, otherwise the name of the archive is appended to the end of the command.  The return code is checked for success (0 on Unix).

       -u
       --update
              Replace (update) an existing entry in the zip archive only if it has been modified more recently than the version already in the zip archive.  For example:

                     zip -u stuff *

              will add any new files in the current directory, and update any files which have been modified since the zip archive stuff.zip was last created/modified (note that zip will not try to pack stuff.zip into itself  when
              you do this).

              Note that the -u option with no input file arguments acts like the -f (freshen) option.

       -U
       --copy-entries
              Copy  entries  from one archive to another.  Requires the --out option to specify a different output file than the input archive.  Copy mode is the reverse of -d delete.  When delete is being used with --out, the se‐
              lected entries are deleted from the archive and all other entries are copied to the new archive, while copy mode selects the files to include in the new archive.  Unlike -u update, input patterns on the command  line
              are matched against archive entries only and not the file system files.  For instance,

                     zip inarchive "*.c" --copy --out outarchive

              copies  entries  with  names ending in .c from inarchive to outarchive.  The wildcard must be escaped on some systems to prevent the shell from substituting names of files from the file system which may have no rele‐
              vance to the entries in the archive.

              If no input files appear on the command line and --out is used, copy mode is assumed:

                     zip inarchive --out outarchive

              This is useful for changing split size for instance.  Encrypting and decrypting entries is not yet supported using copy mode.  Use zipcloak for that.

       -UN v
       --unicode v
              Determine what zip should do with Unicode file names.  zip 3.0, in addition to the standard file path, now includes the UTF-8 translation of the path if the entry path is not entirely 7-bit ASCII.  When an  entry  is
              missing  the Unicode path, zip reverts back to the standard file path.  The problem with using the standard path is this path is in the local character set of the zip that created the entry, which may contain charac‐
              ters that are not valid in the character set being used by the unzip.  When zip is reading an archive, if an entry also has a Unicode path, zip now defaults to using the Unicode path to recreate the standard path us‐
              ing the current local character set.

              This  option  can  be used to determine what zip should do with this path if there is a mismatch between the stored standard path and the stored UTF-8 path (which can happen if the standard path was updated).  In all
              cases, if there is a mismatch it is assumed that the standard path is more current and zip uses that.  Values for v are

                     q - quit if paths do not match

                     w - warn, continue with standard path

                     i - ignore, continue with standard path

                     n - no Unicode, do not use Unicode paths

              The default is to warn and continue.

              Characters that are not valid in the current character set are escaped as #Uxxxx and #Lxxxxxx, where x is an ASCII character for a hex digit.  The first is used if a 16-bit character number is sufficient to represent
              the Unicode character and the second if the character needs more than 16 bits to represent it's Unicode character code.  Setting -UN to

                     e - escape

              as in

                     zip archive -sU -UN=e

              forces zip to escape all characters that are not printable 7-bit ASCII.

              Normally zip stores UTF-8 directly in the standard path field on systems where UTF-8 is the current character set and stores the UTF-8 in the new extra fields otherwise.  The option

                     u - UTF-8

              as in

                     zip archive dir -r -UN=UTF8

              forces  zip  to  store  UTF-8  as native in the archive.  Note that storing UTF-8 directly is the default on Unix systems that support it.  This option could be useful on Windows systems where the escaped path is too
              large to be a valid path and the UTF-8 version of the path is smaller, but native UTF-8 is not backward compatible on Windows systems.

       -v
       --verbose
              Verbose mode or print diagnostic version info.

              Normally, when applied to real operations, this option enables the display of a progress indicator during compression (see -dd for more on dots) and requests verbose diagnostic info about zipfile structure oddities.

              However, when -v is the only command line argument a diagnostic screen is printed instead.  This should now work even if stdout is redirected to a file, allowing easy saving of the information for  sending  with  bug
              reports to Info-ZIP.  The version screen provides the help screen header with program name, version, and release date, some pointers to the Info-ZIP home and distribution sites, and shows information about the target
              environment (compiler type and version, OS version, compilation date and the enabled optional features used to create the zip executable).

       -V
       --VMS-portable
              [VMS] Save VMS file attributes.  (Files are  truncated at EOF.)   When a -V archive is unpacked on a non-VMS system,  some file types (notably Stream_LF text files  and  pure binary files  like fixed-512)  should  be
              extracted intact.  Indexed files and file types with embedded record sizes (notably variable-length record types) will probably be seen as corrupt elsewhere.

       -VV
       --VMS-specific
              [VMS]  Save  VMS  file attributes, and  all allocated blocks in a file,  including  any  data beyond EOF.  Useful for moving ill-formed files  among  VMS systems.   When a -VV archive is unpacked on a non-VMS system,
              almost all files will appear corrupt.

       -w
       --VMS-versions
              [VMS] Append the version number of the files to the name, including multiple versions of files.  Default is to use only the most recent version of a specified file.

       -ww
       --VMS-dot-versions
              [VMS] Append the version number of the files to the name, including multiple versions of files, using the .nnn format.  Default is to use only the most recent version of a specified file.

       -ws
       --wild-stop-dirs
              Wildcards match only at a directory level.  Normally zip handles paths as strings and given the paths

                     /foo/bar/dir/file1.c

                     /foo/bar/file2.c

              an input pattern such as

                     /foo/bar/*

              normally would match both paths, the * matching dir/file1.c and file2.c.  Note that in the first case a directory boundary (/) was crossed in the match.  With -ws no directory bounds will be included  in  the  match,
              making wildcards local to a specific directory level.  So, with -ws enabled, only the second path would be matched.

              When using -ws, use ** to match across directory boundaries as * does normally.

       -x files
       --exclude files
              Explicitly exclude the specified files, as in:

                     zip -r foo foo -x \*.o

              which  will  include  the contents of foo in foo.zip while excluding all the files that end in .o.  The backslash avoids the shell filename substitution, so that the name matching is performed by zip at all directory
              levels.

              Also possible:

                     zip -r foo foo -x@exclude.lst

              which will include the contents of foo in foo.zip while excluding all the files that match the patterns in the file exclude.lst.

              The long option forms of the above are

                     zip -r foo foo --exclude \*.o

              and

                     zip -r foo foo --exclude @exclude.lst

              Multiple patterns can be specified, as in:

                     zip -r foo foo -x \*.o \*.c

              If there is no space between -x and the pattern, just one value is assumed (no list):

                     zip -r foo foo -x\*.o

              See -i for more on include and exclude.

       -X
       --no-extra
              Do not save extra file attributes (Extended Attributes on OS/2, uid/gid and file times on Unix).  The zip format uses extra fields to include additional information for each entry.  Some extra fields are specific  to
              particular  systems  while others are applicable to all systems.  Normally when zip reads entries from an existing archive, it reads the extra fields it knows, strips the rest, and adds the extra fields applicable to
              that system.  With -X, zip strips all old fields and only includes the Unicode and Zip64 extra fields (currently these two extra fields cannot be disabled).

              Negating this option, -X-, includes all the default extra fields, but also copies over any unrecognized extra fields.

       -y
       --symlinks
              For UNIX and VMS (V8.3 and later), store symbolic links as such in the zip archive, instead of compressing and storing the file referred to by the link.  This can avoid multiple copies of files being included in  the
              archive as zip recurses the directory trees and accesses files directly and by links.

       -z
       --archive-comment
              Prompt  for  a  multi-line comment for the entire zip archive.  The comment is ended by a line containing just a period, or an end of file condition (^D on Unix, ^Z on MSDOS, OS/2, and VMS).  The comment can be taken
              from a file:

                     zip -z foo < foowhat

       -Z cm
       --compression-method cm
              Set the default compression method.  Currently the main methods supported by zip are store and deflate.  Compression method can be set to:

              store - Setting the compression method to store forces zip to store entries with no compression.  This is generally faster than compressing entries, but results in no space savings.  This is  the  same  as  using  -0
              (compression level zero).

              deflate - This is the default method for zip.  If zip determines that storing is better than deflation, the entry will be stored instead.

              bzip2  - If bzip2 support is compiled in, this compression method also becomes available.  Only some modern unzips currently support the bzip2 compression method, so test the unzip you will be using before relying on
              archives using this method (compression method 12).

              For example, to add bar.c to archive foo using bzip2 compression:

                     zip -Z bzip2 foo bar.c

              The compression method can be abbreviated:

                     zip -Zb foo bar.c

       -#
       (-0, -1, -2, -3, -4, -5, -6, -7, -8, -9)
              Regulate the speed of compression using the specified digit #, where -0 indicates no compression (store all files), -1 indicates the fastest compression speed (less compression) and -9 indicates the slowest  compres‐
              sion speed (optimal compression, ignores the suffix list). The default compression level is -6.

              Though still being worked, the intention is this setting will control compression speed for all compression methods.  Currently only deflation is controlled.

       -!
       --use-privileges
              [WIN32] Use priviliges (if granted) to obtain all aspects of WinNT security.

       -@
       --names-stdin
              Take the list of input files from standard input. Only one filename per line.

       -$
       --volume-label
              [MSDOS,  OS/2, WIN32] Include the volume label for the drive holding the first file to be compressed.  If you want to include only the volume label or to force a specific drive, use the drive name as first file name,
              as in:

                     zip -$ foo a: c:bar

EXAMPLES
       The simplest example:

              zip stuff *

       creates the archive stuff.zip (assuming it does not exist) and puts all the files in the current directory in it, in compressed form (the .zip suffix is added automatically, unless the archive name contains a  dot  already;
       this allows the explicit specification of other suffixes).

       Because of the way the shell on Unix does filename substitution, files starting with "." are not included; to include these as well:

              zip stuff .* *

       Even this will not include any subdirectories from the current directory.

       To zip up an entire directory, the command:

              zip -r foo foo

       creates the archive foo.zip, containing all the files and directories in the directory foo that is contained within the current directory.

       You may want to make a zip archive that contains the files in foo, without recording the directory name, foo.  You can use the -j option to leave off the paths, as in:

              zip -j foo foo/*

       If  you  are  short on disk space, you might not have enough room to hold both the original directory and the corresponding compressed zip archive.  In this case, you can create the archive in steps using the -m option.  If
       foo contains the subdirectories tom, dick, and harry, you can:

              zip -rm foo foo/tom
              zip -rm foo foo/dick
              zip -rm foo foo/harry

       where the first command creates foo.zip, and the next two add to it.  At the completion of each zip command, the last created archive is deleted, making room for the next zip command to function.

       Use -s to set the split size and create a split archive.  The size is given as a number followed optionally by one of k (kB), m (MB), g (GB), or t (TB).  The command

              zip -s 2g -r split.zip foo

       creates a split archive of the directory foo with splits no bigger than 2 GB each.  If foo contained 5 GB of contents and the contents were stored in the split archive without compression (to make this example simple), this
       would create three splits, split.z01 at 2 GB, split.z02 at 2 GB, and split.zip at a little over 1 GB.

       The -sp option can be used to pause zip between splits to allow changing removable media, for example, but read the descriptions and warnings for both -s and -sp below.

       Though zip does not update split archives, zip provides the new option -O (--output-file) to allow split archives to be updated and saved in a new archive.  For example,

              zip inarchive.zip foo.c bar.c --out outarchive.zip

       reads  archive inarchive.zip, even if split, adds the files foo.c and bar.c, and writes the resulting archive to outarchive.zip.  If inarchive.zip is split then outarchive.zip defaults to the same split size.  Be aware that
       outarchive.zip and any split files that are created with it are always overwritten without warning.  This may be changed in the future.

PATTERN MATCHING
       This section applies only to Unix.  Watch this space for details on MSDOS and VMS operation.  However, the special wildcard characters * and [] below apply to at least MSDOS also.

       The Unix shells (sh, csh, bash, and others) normally do filename substitution (also called "globbing") on command arguments.  Generally the special characters are:

       ?      match any single character

       *      match any number of characters (including none)

       []     match any character in the range indicated within the brackets (example: [a-f], [0-9]).  This form of wildcard matching allows a user to specify a list of characters between square brackets and if any of the  charac‐
              ters match the expression matches.  For example:

                     zip archive "*.[hc]"

              would archive all files in the current directory that end in .h or .c.

              Ranges of characters are supported:

                     zip archive "[a-f]*"

              would add to the archive all files starting with "a" through "f".

              Negation is also supported, where any character in that position not in the list matches.  Negation is supported by adding ! or ^ to the beginning of the list:

                     zip archive "*.[!o]"

              matches files that don't end in ".o".

              On WIN32, [] matching needs to be turned on with the -RE option to avoid the confusion that names with [ or ] have caused.

       When  these characters are encountered (without being escaped with a backslash or quotes), the shell will look for files relative to the current path that match the pattern, and replace the argument with a list of the names
       that matched.

       The zip program can do the same matching on names that are in the zip archive being modified or, in the case of the -x (exclude) or -i (include) options, on the list of files to be  operated  on,  by  using  backslashes  or
       quotes  to  tell  the  shell  not to do the name expansion.  In general, when zip encounters a name in the list of files to do, it first looks for the name in the file system.  If it finds it, it then adds it to the list of
       files to do.  If it does not find it, it looks for the name in the zip archive being modified (if it exists), using the pattern matching characters described above, if present.  For each match, it will add that name to  the
       list of files to be processed, unless this name matches one given with the -x option, or does not match any name given with the -i option.

       The pattern matching includes the path, and so patterns like \*.o match names that end in ".o", no matter what the path prefix is.  Note that the backslash must precede every special character (i.e. ?*[]), or the entire ar‐
       gument must be enclosed in double quotes ("").

       In general, use backslashes or double quotes for paths that have wildcards to make zip do the pattern matching for file paths, and always for paths and strings that have spaces or wildcards for -i, -x, -R, -d,  and  -U  and
       anywhere zip needs to process the wildcards.

ENVIRONMENT
       The following environment variables are read and used by zip as described.

       ZIPOPT
              contains default options that will be used when running zip.  The contents of this environment variable will get added to the command line just after the zip command.

       ZIP
              [Not on RISC OS and VMS] see ZIPOPT

       Zip$Options
              [RISC OS] see ZIPOPT

       Zip$Exts
              [RISC OS] contains extensions separated by a : that will cause native filenames with one of the specified extensions to be added to the zip file with basename and extension swapped.

       ZIP_OPTS
              [VMS] see ZIPOPT

SEE ALSO
       compress(1), shar(1L), tar(1), unzip(1L), gzip(1L)

DIAGNOSTICS
       The exit status (or error level) approximates the exit codes defined by PKWARE and takes on the following values, except under VMS:

              0      normal; no errors or warnings detected.

              2      unexpected end of zip file.

              3      a generic error in the zipfile format was detected.  Processing may have completed successfully anyway; some broken zipfiles created by other archivers have simple work-arounds.

              4      zip was unable to allocate memory for one or more buffers during program initialization.

              5      a severe error in the zipfile format was detected.  Processing probably failed immediately.

              6      entry too large to be processed (such as input files larger than 2 GB when not using Zip64 or trying to read an existing archive that is too large) or entry too large to be split with zipsplit

              7      invalid comment format

              8      zip -T failed or out of memory

              9      the user aborted zip prematurely with control-C (or similar)

              10     zip encountered an error while using a temp file

              11     read or seek error

              12     zip has nothing to do

              13     missing or empty zip file

              14     error writing to a file

              15     zip was unable to create a file to write to

              16     bad command line parameters

              18     zip could not open a specified file to read

              19     zip was compiled with options not supported on this system

       VMS  interprets  standard  Unix (or PC) return values as other, scarier-looking things, so zip instead maps them into VMS-style status codes.  In general, zip sets VMS Facility = 1955 (0x07A3), Code = 2* Unix_status, and an
       appropriate Severity (as specified in ziperr.h).  More details are included in the VMS-specific documentation.  See [.vms]NOTES.TXT and [.vms]vms_msg_gen.c.

BUGS
       zip 3.0 is not compatible with PKUNZIP 1.10. Use zip 1.1 to produce zip files which can be extracted by PKUNZIP 1.10.

       zip files produced by zip 3.0 must not be updated by zip 1.1 or PKZIP 1.10, if they contain encrypted members or if they have been produced in a pipe or on a non-seekable device. The old versions of zip or PKZIP would  cre‐
       ate  an  archive  with an incorrect format.  The old versions can list the contents of the zip file but cannot extract it anyway (because of the new compression algorithm).  If you do not use encryption and use regular disk
       files, you do not have to care about this problem.

       Under VMS, not all of the odd file formats are treated properly.  Only stream-LF format zip files are expected to work with zip.  Others can be converted using Rahul Dhesi's BILF program.  This version of zip  handles  some
       of  the conversion internally.  When using Kermit to transfer zip files from VMS to MSDOS, type "set file type block" on VMS.  When transfering from MSDOS to VMS, type "set file type fixed" on VMS.  In both cases, type "set
       file type binary" on MSDOS.

       Under some older VMS versions, zip may hang for file specifications that use DECnet syntax foo::*.*.

       On OS/2, zip cannot match some names, such as those including an exclamation mark or a hash sign.  This is a bug in OS/2 itself: the 32-bit DosFindFirst/Next don't find such names.  Other programs such as GNU tar  are  also
       affected by this bug.

       Under OS/2, the amount of Extended Attributes displayed by DIR is (for compatibility) the amount returned by the 16-bit version of DosQueryPathInfo(). Otherwise OS/2 1.3 and 2.0 would report different EA sizes when DIRing a
       file.  However, the structure layout returned by the 32-bit DosQueryPathInfo() is a bit different, it uses extra padding bytes and link pointers (it's a linked list) to have all fields on 4-byte boundaries  for  portability
       to  future  RISC  OS/2 versions. Therefore the value reported by zip (which uses this 32-bit-mode size) differs from that reported by DIR.  zip stores the 32-bit format for portability, even the 16-bit MS-C-compiled version
       running on OS/2 1.3, so even this one shows the 32-bit-mode size.

AUTHORS
       Copyright (C) 1997-2008 Info-ZIP.

       Currently distributed under the Info-ZIP license.

       Copyright (C) 1990-1997 Mark Adler, Richard B. Wales, Jean-loup Gailly, Onno van der Linden, Kai Uwe Rommel, Igor Mandrichenko, John Bush and Paul Kienitz.

       Original copyright:

       Permission is granted to any individual or institution to use, copy, or redistribute this software so long as all of the original files are included, that it is not sold for profit, and that this  copyright  notice  is  re‐
       tained.

       LIKE  ANYTHING  ELSE  THAT'S FREE, ZIP AND ITS ASSOCIATED UTILITIES ARE PROVIDED AS IS AND COME WITH NO WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED. IN NO EVENT WILL THE COPYRIGHT HOLDERS BE LIABLE FOR ANY DAMAGES RE‐
       SULTING FROM THE USE OF THIS SOFTWARE.

       Please send bug reports and comments using the web page at: www.info-zip.org.  For bug reports, please include the version of zip (see zip -h), the make options used to compile it (see zip -v),  the  machine  and  operating
       system in use, and as much additional information as possible.

ACKNOWLEDGEMENTS
       Thanks  to R. P. Byrne for his Shrink.Pas program, which inspired this project, and from which the shrink algorithm was stolen; to Phil Katz for placing in the public domain the zip file format, compression format, and .ZIP
       filename extension, and for accepting minor changes to the file format; to Steve Burg for clarifications on the deflate format; to Haruhiko Okumura and Leonid Broukhis for providing some useful ideas for the compression al‐
       gorithm;  to  Keith  Petersen,  Rich  Wales,  Hunter Goatley and Mark Adler for providing a mailing list and ftp site for the Info-ZIP group to use; and most importantly, to the Info-ZIP group itself (listed in the file in‐
       fozip.who) without whose tireless testing and bug-fixing efforts a portable zip would not have been possible.  Finally we should thank (blame) the first Info-ZIP moderator, David Kirschbaum, for getting us into this mess in
       the first place.  The manual page was rewritten for Unix by R. P. C. Rodgers and updated by E. Gordon for zip 3.0.

Info-ZIP                                                                                                  16 June 2008 (v3.0)                                                                                                  ZIP(1L)
bzip2(1)                                                                                                General Commands Manual                                                                                               bzip2(1)

NAME
       bzip2, bunzip2 - a block-sorting file compressor, v1.0.8
       bzcat - decompresses files to stdout
       bzip2recover - recovers data from damaged bzip2 files

SYNOPSIS
       bzip2 [ -cdfkqstvzVL123456789 ] [ filenames ...  ]
       bunzip2 [ -fkvsVL ] [ filenames ...  ]
       bzcat [ -s ] [ filenames ...  ]
       bzip2recover filename

DESCRIPTION
       bzip2  compresses  files using the Burrows-Wheeler block sorting text compression algorithm, and Huffman coding.  Compression is generally considerably better than that achieved by more conventional LZ77/LZ78-based compres‐
       sors, and approaches the performance of the PPM family of statistical compressors.

       The command-line options are deliberately very similar to those of GNU gzip, but they are not identical.

       bzip2 expects a list of file names to accompany the command-line flags.  Each file is replaced by a compressed version of itself, with the name "original_name.bz2".  Each compressed file has the same modification date, per‐
       missions,  and, when possible, ownership as the corresponding original, so that these properties can be correctly restored at decompression time.  File name handling is naive in the sense that there is no mechanism for pre‐
       serving original file names, permissions, ownerships or dates in filesystems which lack these concepts, or have serious file name length restrictions, such as MS-DOS.

       bzip2 and bunzip2 will by default not overwrite existing files.  If you want this to happen, specify the -f flag.

       If no file names are specified, bzip2 compresses from standard input to standard output.  In this case, bzip2 will decline to write compressed output to a terminal, as this would be entirely incomprehensible  and  therefore
       pointless.

       bunzip2 (or bzip2 -d) decompresses all specified files.  Files which were not created by bzip2 will be detected and ignored, and a warning issued.  bzip2 attempts to guess the filename for the decompressed file from that of
       the compressed file as follows:

              filename.bz2    becomes   filename
              filename.bz     becomes   filename
              filename.tbz2   becomes   filename.tar
              filename.tbz    becomes   filename.tar
              anyothername    becomes   anyothername.out

       If the file does not end in one of the recognised endings, .bz2, .bz, .tbz2 or .tbz, bzip2 complains that it cannot guess the name of the original file, and uses the original name with .out appended.

       As with compression, supplying no filenames causes decompression from standard input to standard output.

       bunzip2 will correctly decompress a file which is the concatenation of two or more compressed files.  The result is the concatenation of the corresponding uncompressed files.  Integrity testing  (-t)  of  concatenated  com‐
       pressed files is also supported.

       You  can  also  compress or decompress files to the standard output by giving the -c flag.  Multiple files may be compressed and decompressed like this.  The resulting outputs are fed sequentially to stdout.  Compression of
       multiple files in this manner generates a stream containing multiple compressed file representations.  Such a stream can be decompressed correctly only by bzip2 version 0.9.0 or later.  Earlier versions of bzip2  will  stop
       after decompressing the first file in the stream.

       bzcat (or bzip2 -dc) decompresses all specified files to the standard output.

       bzip2 will read arguments from the environment variables BZIP2 and BZIP, in that order, and will process them before any arguments read from the command line.  This gives a convenient way to supply default arguments.

       Compression  is  always performed, even if the compressed file is slightly larger than the original.  Files of less than about one hundred bytes tend to get larger, since the compression mechanism has a constant overhead in
       the region of 50 bytes.  Random data (including the output of most file compressors) is coded at about 8.05 bits per byte, giving an expansion of around 0.5%.

       As a self-check for your protection, bzip2 uses 32-bit CRCs to make sure that the decompressed version of a file is identical to the original.  This guards against corruption of the compressed data, and  against  undetected
       bugs  in  bzip2  (hopefully very unlikely).  The chances of data corruption going undetected is microscopic, about one chance in four billion for each file processed.  Be aware, though, that the check occurs upon decompres‐
       sion, so it can only tell you that something is wrong.  It can't help you recover the original uncompressed data.  You can use bzip2recover to try to recover data from damaged files.

       Return values: 0 for a normal exit, 1 for environmental problems (file not found, invalid flags, I/O errors, &c), 2 to indicate a corrupt compressed file, 3 for an internal consistency error (eg, bug) which caused bzip2  to
       panic.

OPTIONS
       -c --stdout
              Compress or decompress to standard output.

       -d --decompress
              Force  decompression.   bzip2,  bunzip2  and  bzcat are really the same program, and the decision about what actions to take is done on the basis of which name is used.  This flag overrides that mechanism, and forces
              bzip2 to decompress.

       -z --compress
              The complement to -d: forces compression, regardless of the invocation name.

       -t --test
              Check integrity of the specified file(s), but don't decompress them.  This really performs a trial decompression and throws away the result.

       -f --force
              Force overwrite of output files.  Normally, bzip2 will not overwrite existing output files.  Also forces bzip2 to break hard links to files, which it otherwise wouldn't do.

              bzip2 normally declines to decompress files which don't have the correct magic header bytes.  If forced (-f), however, it will pass such files through unmodified.  This is how GNU gzip behaves.

       -k --keep
              Keep (don't delete) input files during compression or decompression.

       -s --small
              Reduce memory usage, for compression, decompression and testing.  Files are decompressed and tested using a modified algorithm which only requires 2.5 bytes per block byte.  This means any file can be decompressed in
              2300k of memory, albeit at about half the normal speed.

              During compression, -s selects a block size of 200k, which limits memory use to around the same figure, at the expense of your compression ratio.  In short, if your machine is low on memory (8 megabytes or less), use
              -s for everything.  See MEMORY MANAGEMENT below.

       -q --quiet
              Suppress non-essential warning messages.  Messages pertaining to I/O errors and other critical events will not be suppressed.

       -v --verbose
              Verbose mode -- show the compression ratio for each file processed.  Further -v's increase the verbosity level, spewing out lots of information which is primarily of interest for diagnostic purposes.

       -L --license -V --version
              Display the software version, license terms and conditions.

       -1 (or --fast) to -9 (or --best)
              Set the block size to 100 k, 200 k ..  900 k when compressing.  Has no effect when decompressing.  See MEMORY MANAGEMENT below.  The --fast and --best aliases are primarily for GNU gzip compatibility.  In particular,
              --fast doesn't make things significantly faster.  And --best merely selects the default behaviour.

       --     Treats all subsequent arguments as file names, even if they start with a dash.  This is so you can handle files with names beginning with a dash, for example: bzip2 -- -myfilename.

       --repetitive-fast --repetitive-best
              These flags are redundant in versions 0.9.5 and above.  They provided some coarse control over the behaviour of the sorting algorithm in earlier versions, which was sometimes useful.  0.9.5 and above have an improved
              algorithm which renders these flags irrelevant.

MEMORY MANAGEMENT
       bzip2 compresses large files in blocks.  The block size affects both the compression ratio achieved, and the amount of memory needed for compression and decompression.  The flags -1 through -9 specify the block size  to  be
       100,000  bytes through 900,000 bytes (the default) respectively.  At decompression time, the block size used for compression is read from the header of the compressed file, and bunzip2 then allocates itself just enough mem‐
       ory to decompress the file.  Since block sizes are stored in compressed files, it follows that the flags -1 to -9 are irrelevant to and so ignored during decompression.

       Compression and decompression requirements, in bytes, can be estimated as:

              Compression:   400k + ( 8 x block size )

              Decompression: 100k + ( 4 x block size ), or
                             100k + ( 2.5 x block size )

       Larger block sizes give rapidly diminishing marginal returns.  Most of the compression comes from the first two or three hundred k of block size, a fact worth bearing in mind when using bzip2 on small machines.  It is  also
       important to appreciate that the decompression memory requirement is set at compression time by the choice of block size.

       For  files compressed with the default 900k block size, bunzip2 will require about 3700 kbytes to decompress.  To support decompression of any file on a 4 megabyte machine, bunzip2 has an option to decompress using approxi‐
       mately half this amount of memory, about 2300 kbytes.  Decompression speed is also halved, so you should use this option only where necessary.  The relevant flag is -s.

       In general, try and use the largest block size memory constraints allow, since that maximises the compression achieved.  Compression and decompression speed are virtually unaffected by block size.

       Another significant point applies to files which fit in a single block -- that means most files you'd encounter using a large block size.  The amount of real memory touched is proportional to the size of the file, since the
       file is smaller than a block.  For example, compressing a file 20,000 bytes long with the flag -9 will cause the compressor to allocate around 7600k of memory, but only touch 400k + 20000 * 8 = 560 kbytes of it.  Similarly,
       the decompressor will allocate 3700k but only touch 100k + 20000 * 4 = 180 kbytes.

       Here is a table which summarises the maximum memory usage for different block sizes.  Also recorded is the total compressed size for 14 files of the Calgary Text Compression Corpus totalling 3,141,622  bytes.   This  column
       gives some feel for how compression varies with block size.  These figures tend to understate the advantage of larger block sizes for larger files, since the Corpus is dominated by smaller files.

                  Compress   Decompress   Decompress   Corpus
           Flag     usage      usage       -s usage     Size

            -1      1200k       500k         350k      914704
            -2      2000k       900k         600k      877703
            -3      2800k      1300k         850k      860338
            -4      3600k      1700k        1100k      846899
            -5      4400k      2100k        1350k      845160
            -6      5200k      2500k        1600k      838626
            -7      6100k      2900k        1850k      834096
            -8      6800k      3300k        2100k      828642
            -9      7600k      3700k        2350k      828642

RECOVERING DATA FROM DAMAGED FILES
       bzip2 compresses files in blocks, usually 900kbytes long.  Each block is handled independently.  If a media or transmission error causes a multi-block .bz2 file to become damaged, it may be possible to recover data from the
       undamaged blocks in the file.

       The compressed representation of each block is delimited by a 48-bit pattern, which makes it possible to find the block boundaries with reasonable certainty.  Each block also carries its own 32-bit CRC,  so  damaged  blocks
       can be distinguished from undamaged ones.

       bzip2recover  is a simple program whose purpose is to search for blocks in .bz2 files, and write each block out into its own .bz2 file.  You can then use bzip2 -t to test the integrity of the resulting files, and decompress
       those which are undamaged.

       bzip2recover takes a single argument, the name of the damaged file, and writes a number of files "rec00001file.bz2", "rec00002file.bz2", etc, containing the  extracted  blocks.  The  output   filenames   are   designed   so
       that the use of wildcards in subsequent processing -- for example, "bzip2 -dc  rec*file.bz2 > recovered_data" -- processes the files in the correct order.

       bzip2recover  should be of most use dealing with large .bz2 files,  as  these will contain many blocks.  It is clearly futile to use it on damaged single-block  files,  since  a damaged  block  cannot  be recovered.  If you
       wish to minimise any potential data loss through media  or  transmission errors, you might consider compressing with a smaller block size.

PERFORMANCE NOTES
       The sorting phase of compression gathers together similar strings in the file.  Because of this, files containing very long runs of repeated symbols, like "aabaabaabaab ..."  (repeated several hundred  times)  may  compress
       more  slowly  than normal.  Versions 0.9.5 and above fare much better than previous versions in this respect.  The ratio between worst-case and average-case compression time is in the region of 10:1.  For previous versions,
       this figure was more like 100:1.  You can use the -vvvv option to monitor progress in great detail, if you want.

       Decompression speed is unaffected by these phenomena.

       bzip2 usually allocates several megabytes of memory to operate in, and then charges all over it in a fairly random fashion.  This means that performance, both for compressing and decompressing, is largely determined by  the
       speed  at  which your machine can service cache misses.  Because of this, small changes to the code to reduce the miss rate have been observed to give disproportionately large performance improvements.  I imagine bzip2 will
       perform best on machines with very large caches.

CAVEATS
       I/O error messages are not as helpful as they could be.  bzip2 tries hard to detect I/O errors and exit cleanly, but the details of what the problem is sometimes seem rather misleading.

       This manual page pertains to version 1.0.8 of bzip2.  Compressed data created by this version is entirely forwards and backwards compatible with the previous public releases, versions 0.1pl2,  0.9.0,  0.9.5,  1.0.0,  1.0.1,
       1.0.2 and above, but with the following exception: 0.9.0 and above can correctly decompress multiple concatenated compressed files.  0.1pl2 cannot do this; it will stop after decompressing just the first file in the stream.

       bzip2recover  versions prior to 1.0.2 used 32-bit integers to represent bit positions in compressed files, so they could not handle compressed files more than 512 megabytes long.  Versions 1.0.2 and above use 64-bit ints on
       some platforms which support them (GNU supported targets, and Windows).  To establish whether or not bzip2recover was built with such a limitation, run it without arguments.  In any event you can build yourself an unlimited
       version if you can recompile it with MaybeUInt64 set to be an unsigned 64-bit integer.

AUTHOR
       Julian Seward, jseward@acm.org.

       https://sourceware.org/bzip2/

       The  ideas  embodied in bzip2 are due to (at least) the following people: Michael Burrows and David Wheeler (for the block sorting transformation), David Wheeler (again, for the Huffman coder), Peter Fenwick (for the struc‐
       tured coding model in the original bzip, and many refinements), and Alistair Moffat, Radford Neal and Ian Witten (for the arithmetic coder in the original bzip).  I am much indebted for their help, support and advice.   See
       the manual in the source distribution for pointers to sources of documentation.  Christian von Roques encouraged me to look for faster sorting algorithms, so as to speed up compression.  Bela Lubkin encouraged me to improve
       the worst-case compression performance.  Donna Robinson XMLised the documentation.  The bz* scripts are derived from those of GNU gzip.  Many people sent patches, helped with portability problems, lent machines, gave advice
       and were generally helpful.

                                                                                                                                                                                                                              bzip2(1)
