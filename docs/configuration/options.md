Configuration options for isort
========

As a code formatter isort has opinions. However, it also allows you to have your own. If your opinions disagree with those of isort,
isort will disagree but commit to your way of formatting. To enable this, isort exposes a plethora of options to specify
how you want your imports sorted, organized, and formatted.


## Python Version
Tells isort to set the known standard library based on the the specified Python version. Default is to assume any Python 3 version could be the target, and use a union off all stdlib modules across versions. If auto is specified, the version of the interpreter used to run isort (currently: 38) will be used.

**Type:** String  
**Default:** `py3`  
**Python & Config File Name:** py_version  
**CLI Flags:**

 - --py
 - --python-version

## Force To Top
Force specific imports to the top of their appropriate section.

**Type:** Frozenset  
**Default:** `frozenset()`  
**Python & Config File Name:** force_to_top  
**CLI Flags:**

 - -t
 - --top

## Skip
Files that sort imports should skip over. If you want to skip multiple files you should specify twice: --skip file1 --skip file2.

**Type:** Frozenset  
**Default:** `frozenset({'.nox', 'node_modules', 'buck-out', '.venv', '.mypy_cache', 'build', '.pants.d', '.hg', 'dist', '.git', '_build', '.eggs', 'venv', '.tox'})`  
**Python & Config File Name:** skip  
**CLI Flags:**

 - -s
 - --skip

## Skip Glob
Files that sort imports should skip over.

**Type:** Frozenset  
**Default:** `frozenset()`  
**Python & Config File Name:** skip_glob  
**CLI Flags:**

 - --sg
 - --skip-glob

## Line Length
The max length of an import line (used for wrapping long imports).

**Type:** Int  
**Default:** `79`  
**Python & Config File Name:** line_length  
**CLI Flags:**

 - -l
 - -w
 - --line-length
 - --line-width

## Wrap Length
Specifies how long lines that are wrapped should be, if not set line_length is used.
NOTE: wrap_length must be LOWER than or equal to line_length.

**Type:** Int  
**Default:** `0`  
**Python & Config File Name:** wrap_length  
**CLI Flags:**

 - --wl
 - --wrap-length

## Line Ending
Forces line endings to the specified value. If not set, values will be guessed per-file.

**Type:** String  
**Default:** ``  
**Python & Config File Name:** line_ending  
**CLI Flags:**

 - --le
 - --line-ending

## Sections
**No Description**

**Type:** Tuple  
**Default:** `('FUTURE', 'STDLIB', 'THIRDPARTY', 'FIRSTPARTY', 'LOCALFOLDER')`  
**Python & Config File Name:** sections  
**CLI Flags:**

 - **Not Supported**

## No Sections
Put all imports into the same section bucket

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** no_sections  
**CLI Flags:**

 - --ds
 - --no-sections

## Known Future Library
Force isort to recognize a module as part of the future compatibility libraries.

**Type:** Frozenset  
**Default:** `frozenset({'__future__'})`  
**Python & Config File Name:** known_future_library  
**CLI Flags:**

 - -f
 - --future

## Known Third Party
Force isort to recognize a module as being part of a third party library.

**Type:** Frozenset  
**Default:** `frozenset({'google.appengine.api'})`  
**Python & Config File Name:** known_third_party  
**CLI Flags:**

 - -o
 - --thirdparty

## Known First Party
Force isort to recognize a module as being part of the current python project.

**Type:** Frozenset  
**Default:** `frozenset()`  
**Python & Config File Name:** known_first_party  
**CLI Flags:**

 - -p
 - --project

## Known Standard Library
Force isort to recognize a module as part of the python standard library.

**Type:** Frozenset  
**Default:** `frozenset({'multiprocessing', 'codeop', 'pprint', 'chunk', 'msilib', 'concurrent', 'sched', 'random', 'webbrowser', 'socketserver', 'nis', 'tracemalloc', 'filecmp', 'formatter', 'codecs', 'winsound', 'tty', 'xml', 'gzip', 'binascii', 'enum', 'symtable', '_thread', 'xmlrpc', 'io', 'timeit', 'typing', 'datetime', 'sysconfig', 'ipaddress', 'traceback', 'zipfile', 'audioop', 'mimetypes', 'poplib', 'glob', 'weakref', 'pdb', 'locale', 'queue', 'collections', '_dummy_thread', 'trace', 'linecache', 'code', 'wave', 'reprlib', 'zipimport', 'posix', 'select', 'time', 'sqlite3', 'cgitb', 'ast', 'imp', 'shutil', 'resource', 'decimal', 'itertools', 'json', 'curses', 'pkgutil', 'contextvars', 'bdb', 'dis', 'pstats', 'copyreg', 'distutils', 'marshal', 'winreg', 'faulthandler', 'nntplib', 'ssl', 'struct', 'functools', 'pydoc', 'stat', 'asyncore', 'runpy', 'token', 'ossaudiodev', 'shlex', 'urllib', 'cgi', 'imghdr', 'netrc', 'operator', 'py_compile', 'unittest', 'sunau', 'tempfile', 'textwrap', 'dbm', 'calendar', 'cmath', 'selectors', 'dataclasses', 'pickletools', 'macpath', 'pipes', 'pyclbr', 'asyncio', 'copy', 'spwd', 'heapq', 'statistics', 'venv', 'optparse', 'string', 'encodings', 'fnmatch', 'ftplib', 'bisect', 'fractions', 'msvcrt', 'html', 'binhex', 'crypt', 'colorsys', 'telnetlib', 'smtplib', 'ctypes', 'stringprep', 'fpectl', 'warnings', 'atexit', 'signal', 'subprocess', 'aifc', 'getpass', 'ensurepip', 'imaplib', 'gc', 'profile', 'parser', 'math', 'errno', 'numbers', 'readline', 'argparse', 'mailbox', 'smtpd', 'zlib', 'os', 'platform', 'tarfile', 'tkinter', 'configparser', 'plistlib', 'keyword', 'pathlib', 'mailcap', 'lzma', 'cProfile', 'sndhdr', 'secrets', 'mmap', 'array', 'pickle', 'syslog', 'threading', 'xdrlib', 'http', 'socket', 'tabnanny', 'email', 'rlcompleter', 'logging', 'inspect', 'test', 'quopri', 'difflib', 'bz2', 'types', 'csv', 'gettext', 'dummy_threading', 'symbol', 'turtledemo', 'compileall', 'hmac', 'doctest', 'unicodedata', 'turtle', 'uuid', 'sys', 'termios', 'modulefinder', 'contextlib', 'tokenize', 'zipapp', 're', 'cmd', 'uu', 'base64', 'fileinput', 'wsgiref', 'getopt', 'grp', 'lib2to3', 'pwd', 'site', 'asynchat', 'shelve', 'pty', 'builtins', 'fcntl', 'importlib', 'abc', 'hashlib'})`  
**Python & Config File Name:** known_standard_library  
**CLI Flags:**

 - -b
 - --builtin

## Known Other
**No Description**

**Type:** Dict  
**Default:** `{}`  
**Python & Config File Name:** known_other  
**CLI Flags:**

 - **Not Supported**

## Multi Line Output
Multi line output (0-grid, 1-vertical, 2-hanging, 3-vert-hanging, 4-vert-grid, 5-vert-grid-grouped, 6-vert-grid-grouped-no-comma).

**Type:** Wrapmodes  
**Default:** `WrapModes.GRID`  
**Python & Config File Name:** multi_line_output  
**CLI Flags:**

 - -m
 - --multi-line

## Forced Separate
**No Description**

**Type:** Tuple  
**Default:** `()`  
**Python & Config File Name:** forced_separate  
**CLI Flags:**

 - **Not Supported**

## Indent
String to place for indents defaults to "    " (4 spaces).

**Type:** String  
**Default:** `    `  
**Python & Config File Name:** indent  
**CLI Flags:**

 - -i
 - --indent

## Comment Prefix
**No Description**

**Type:** String  
**Default:** `  #`  
**Python & Config File Name:** comment_prefix  
**CLI Flags:**

 - **Not Supported**

## Length Sort
Sort imports by their string length.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** length_sort  
**CLI Flags:**

 - --ls
 - --length-sort

## Length Sort Sections
**No Description**

**Type:** Frozenset  
**Default:** `frozenset()`  
**Python & Config File Name:** length_sort_sections  
**CLI Flags:**

 - **Not Supported**

## Add Imports
Adds the specified import line to all files, automatically determining correct placement.

**Type:** Frozenset  
**Default:** `frozenset()`  
**Python & Config File Name:** add_imports  
**CLI Flags:**

 - -a
 - --add-import

## Remove Imports
Removes the specified import from all files.

**Type:** Frozenset  
**Default:** `frozenset()`  
**Python & Config File Name:** remove_imports  
**CLI Flags:**

 - --rm
 - --remove-import

## Reverse Relative
Reverse order of relative imports.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** reverse_relative  
**CLI Flags:**

 - --rr
 - --reverse-relative

## Force Single Line
Forces all from imports to appear on their own line

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** force_single_line  
**CLI Flags:**

 - --sl
 - --force-single-line-imports

## Single Line Exclusions
One or more modules to exclude from the single line rule.

**Type:** Tuple  
**Default:** `()`  
**Python & Config File Name:** single_line_exclusions  
**CLI Flags:**

 - --nsl
 - --single-line-exclusions

## Default Section
Sets the default section for imports (by default FIRSTPARTY) options: ('FUTURE', 'STDLIB', 'THIRDPARTY', 'FIRSTPARTY', 'LOCALFOLDER')

**Type:** String  
**Default:** `FIRSTPARTY`  
**Python & Config File Name:** default_section  
**CLI Flags:**

 - --sd
 - --section-default

## Import Headings
**No Description**

**Type:** Dict  
**Default:** `{}`  
**Python & Config File Name:** import_headings  
**CLI Flags:**

 - **Not Supported**

## Balanced Wrapping
Balances wrapping to produce the most consistent line length possible

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** balanced_wrapping  
**CLI Flags:**

 - -e
 - --balanced

## Use Parentheses
Use parenthesis for line continuation on length limit instead of slashes.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** use_parentheses  
**CLI Flags:**

 - --up
 - --use-parentheses

## Order By Type
Order imports by type in addition to alphabetically

**Type:** Bool  
**Default:** `True`  
**Python & Config File Name:** order_by_type  
**CLI Flags:**

 - --ot
 - --order-by-type

## Atomic
Ensures the output doesn't save if the resulting file contains syntax errors.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** atomic  
**CLI Flags:**

 - --ac
 - --atomic

## Lines After Imports
**No Description**

**Type:** Int  
**Default:** `-1`  
**Python & Config File Name:** lines_after_imports  
**CLI Flags:**

 - --lai
 - --lines-after-imports

## Lines Between Sections
**No Description**

**Type:** Int  
**Default:** `1`  
**Python & Config File Name:** lines_between_sections  
**CLI Flags:**

 - **Not Supported**

## Lines Between Types
**No Description**

**Type:** Int  
**Default:** `0`  
**Python & Config File Name:** lines_between_types  
**CLI Flags:**

 - --lbt
 - --lines-between-types

## Combine As Imports
Combines as imports on the same line.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** combine_as_imports  
**CLI Flags:**

 - --ca
 - --combine-as

## Combine Star
Ensures that if a star import is present, nothing else is imported from that namespace.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** combine_star  
**CLI Flags:**

 - --cs
 - --combine-star

## Keep Direct And As Imports
Turns off default behavior that removes direct imports when as imports exist.

**Type:** Bool  
**Default:** `True`  
**Python & Config File Name:** keep_direct_and_as_imports  
**CLI Flags:**

 - -k
 - --keep-direct-and-as

## Include Trailing Comma
Includes a trailing comma on multi line imports that include parentheses.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** include_trailing_comma  
**CLI Flags:**

 - --tc
 - --trailing-comma

## From First
Switches the typical ordering preference, showing from imports first then straight ones.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** from_first  
**CLI Flags:**

 - --ff
 - --from-first

## Verbose
Shows verbose output, such as when files are skipped or when a check is successful.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** verbose  
**CLI Flags:**

 - -v
 - --verbose

## Quiet
Shows extra quiet output, only errors are outputted.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** quiet  
**CLI Flags:**

 - -q
 - --quiet

## Force Adds
Forces import adds even if the original file is empty.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** force_adds  
**CLI Flags:**

 - --af
 - --force-adds

## Force Alphabetical Sort Within Sections
**No Description**

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** force_alphabetical_sort_within_sections  
**CLI Flags:**

 - **Not Supported**

## Force Alphabetical Sort
Force all imports to be sorted alphabetically within a section

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** force_alphabetical_sort  
**CLI Flags:**

 - --fass
 - --force-alphabetical-sort-within-sections

## Force Grid Wrap
Force number of from imports (defaults to 2) to be grid wrapped regardless of line length

**Type:** Int  
**Default:** `0`  
**Python & Config File Name:** force_grid_wrap  
**CLI Flags:**

 - --fgw
 - --force-grid-wrap

## Force Sort Within Sections
Force imports to be sorted by module, independent of import_type

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** force_sort_within_sections  
**CLI Flags:**

 - --fss
 - --force-sort-within-sections

## Lexicographical
**No Description**

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** lexicographical  
**CLI Flags:**

 - **Not Supported**

## Ignore Whitespace
Tells isort to ignore whitespace differences when --check-only is being used.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** ignore_whitespace  
**CLI Flags:**

 - --ws
 - --ignore-whitespace

## No Lines Before
Sections which should not be split with previous by empty lines

**Type:** Frozenset  
**Default:** `frozenset()`  
**Python & Config File Name:** no_lines_before  
**CLI Flags:**

 - --nlb
 - --no-lines-before

## No Inline Sort
Leaves `from` imports with multiple imports 'as-is' (e.g. `from foo import a, c ,b`).

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** no_inline_sort  
**CLI Flags:**

 - --nis
 - --no-inline-sort

## Ignore Comments
**No Description**

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** ignore_comments  
**CLI Flags:**

 - **Not Supported**

## Case Sensitive
Tells isort to include casing when sorting module names

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** case_sensitive  
**CLI Flags:**

 - --case-sensitive

## Sources
**No Description**

**Type:** Tuple  
**Default:** `()`  
**Python & Config File Name:** sources  
**CLI Flags:**

 - **Not Supported**

## Virtual Env
Virtual environment to use for determining whether a package is third-party

**Type:** String  
**Default:** ``  
**Python & Config File Name:** virtual_env  
**CLI Flags:**

 - --virtual-env

## Conda Env
Conda environment to use for determining whether a package is third-party

**Type:** String  
**Default:** ``  
**Python & Config File Name:** conda_env  
**CLI Flags:**

 - --conda-env

## Ensure Newline Before Comments
Inserts a blank line before a comment following an import.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** ensure_newline_before_comments  
**CLI Flags:**

 - -n
 - --ensure-newline-before-comments

## Directory
**No Description**

**Type:** String  
**Default:** ``  
**Python & Config File Name:** directory  
**CLI Flags:**

 - **Not Supported**

## Profile
Base profile type to use for configuration.

**Type:** String  
**Default:** ``  
**Python & Config File Name:** profile  
**CLI Flags:**

 - --profile

## Src Paths
**No Description**

**Type:** Frozenset  
**Default:** `frozenset()`  
**Python & Config File Name:** src_paths  
**CLI Flags:**

 - **Not Supported**

## Old Finders
Use the old deprecated finder logic that relies on environment introspection magic.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** old_finders  
**CLI Flags:**

 - --old-finders
 - --magic

## Source Paths
Add an explicitly defined source path (modules within src paths have their imports automatically catorgorized as first_party).

**Type:** String  
**Default:** `None`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - --src
 - --src-path

## Check
Checks the file for unsorted / unformatted imports and prints them to the command line without modifying the file.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - -c
 - --check-only
 - --check

## Write To Stdout
Force resulting output to stdout, instead of in-place.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - -d
 - --stdout

## Show Diff
Prints a diff of all the changes isort would make to a file, instead of changing it in place

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - --df
 - --diff

## Jobs
Number of files to process in parallel.

**Type:** Int  
**Default:** `None`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - -j
 - --jobs

## Dont Order By Type
Don't order imports by type in addition to alphabetically

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - --dt
 - --dont-order-by-type

## Settings Path
Explicitly set the settings path or file instead of auto determining based on file location.

**Type:** String  
**Default:** `None`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - --sp
 - --settings-path
 - --settings-file
 - --settings

## Show Version
Displays the currently installed version of isort.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - -V
 - --version

## Version Number
Returns just the current version number without the logo

**Type:** String  
**Default:** `==SUPPRESS==`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - --vn
 - --version-number

## Filter Files
Tells isort to filter files even when they are explicitly passed in as part of the command

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - --filter-files

## Files
One or more Python source files that need their imports sorted.

**Type:** String  
**Default:** `None`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - 

## Ask To Apply
Tells isort to apply changes interactively.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - --interactive

## Show Config
See isort's determined config, as well as sources of config options.

**Type:** Bool  
**Default:** `False`  
**Python & Config File Name:** **Not Supported**  
**CLI Flags:**

 - --show-config
