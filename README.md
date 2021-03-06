# finddup
Python utility to find duplicate regular files

Written for python3


## Usage
~~~~
Usage: cmd_handler.py [OPTION]... [FILE]...
Finds duplicate regular files in FILEs and outputs them in groups
Each FILE can a path to a directory or a file
If no FILE is provided current working directory is used
Given FILEs will not be filtered out given any OPTION
Ignores all symlinks

Options:
  -h, --help            show this help message and exit
  -r, --recurse         Recursively check files in subdirectories
  -a, --all             Include directories and files begining with .
  -v, --verbose         Output all errors to stderr as they occour (disabled
                        by default)
  -s SORT, --sort=SORT  Sort group by size: ASCE for ascending. DESC for
                        decending
  --lsize               List file size of a single file in each group along
                        with the groups
  --lsizef=MODE         If --lsize if given; list file size in format MODE
                        (defaults to bytes) as follows; k (kilobytes), m
                        (megabytes)
  --minsize=MIN_SIZE    Only check files with byte size atleast MIN (MIN = 0
                        is ignored)
  --maxsize=MAX_SIZE    Only check files with byte size at most MAX (MAX = 0
                        is ignored)
  --alg=ALG             Use one of the following algorithms to establish file
                        equivalence (defaults to md5): md5 sha1 sha224 sha256
                        sha384 sha512 <+ algs depending on OpenSSL lib used
                        by Python (due to hashlib.py)>
~~~~
