Counts the number of lines of code in a php folder.

Place code_stats.php somewhere in your php project.

Edit the variables at the top of the file to fit your needs. Default values:

    $file_types = array('php','js','scss');
    $skip_directories = array('.git', 'files', 'external', 'scripts');
    $starting_directory = '../';

* file_types are the file types to include in the count
* skip_directories are the names of directories to be skipped. Only accepts names not paths at this time. Example '.git' will skipp the entire .git directory. However '/files/cache' will not work correctly. Also if multiple directories have the same name both will be skipped. 
* starting_directory - The root directory to pull the files from. The script will start at this directory and recursivly search all directories not in the exclude list.

Stats

* Total Lines = Total lines in the included files.
* Ajdusted Lines = Total Lines - Commented Lines - Blank Lines - Braket Lines
* Commented Lines = Lines that are inside of a comment block (/* comment */) or begin with a comment syntax (//). lines that are code followed by line type comments will not be considered comment lines (int k = 5 // # of weekdays.). 
* Blank Lines = lines with only white space characters.
* Bracket lines = lines that include only { or } and nothing else.
* Comment Blocks = Blocks that begin with /* and end with */ accross multiple lines. single line comment blocks are not yet supported.
* Classes = lines that begin with the word "class"
* functions = lines that begin with the word "function"

Known bugs

* Block type comments on a single line are not supported (/* */). Multi line block comments are.

Example Output:

Total lines: 55674
Adjusted lines: 33853
Commented_lines: 5268
Blank_lines: 6152
Bracket_lines: 10401
Comment_blocks: 404
Classes: 51
Functions: 937

Included Files (342): 
C:\Sites\scheduler.local/index.php
C:\Sites\scheduler.local\libraries\db/database.lib.php
C:\Sites\scheduler.local\libraries\db/mysql.lib.php
C:\Sites\scheduler.local\libraries\db/sqlserver.lib.php
C:\Sites\scheduler.local\libraries\form/form.lib.php
C:\Sites\scheduler.local\libraries\form\form_items/form_item.lib.php

Excluded Files & Directories (107): 
C:\Sites\scheduler.local/.git
C:\Sites\scheduler.local/.gitignore
C:\Sites\scheduler.local/.htaccess
C:\Sites\scheduler.local\.idea/.name
