# Bash Commands You Should Know

## File System

### Concepts

#### Full Paths
* Begin with `/`
* Examples
  * `/full/path/to/file`
  * `/home/kim/dev/hello-world.txt`

#### Relative Paths
* Do not begin with a `/`
* Reference files or directories relative to the current directory
* Examples
  * `relative/path/to/file`
  * `../relative/path/to/file` - `../` - Reference the parent directory
  * `../../../relative/path/to/file` - Reference the parent of the parent of the parent directory

#### Current Directory
* `.` references the current directory
* Examples
  * `./some-file` - Reference the file `some-file` in the current directory
  * `ls .` - List the files in the current directory

#### Parent Directories
* `../` references the parent directory
* You can use multiples (`../../../`) to reference a directory multiple levels above
* Examples
  * `../some-file` - Reference the file `some-file` which exists one directory above the current directory
  * `ls ../../../` - List the contents of the directory three levels above the current directory

### Commands

#### `cd [path_to_directory]`
* What does it do?
  * Change directory
* Examples
  * `cd` - Change to home directory
  * `cd /full/path/to/dir` - Change to the specified directory
  * `cd relative/path/to/dir`
  * `cd ..` - Change to parent directory
  * `cd ../../../relative/path/to/dir` - Change to specified directory, with each `../` indicating a parent directory

#### `ls [path_to_directory]`
* What does it do?
  * List the contents of a directory
  * Does not inherently list hidden files
* Examples
  * `ls` - List contents of current directory
  * `ls /full/path/to/dir` - List contents of specified directory
  * `ls relative/path/to/dir`
  * `ls -la` - List all contents of current directory (including hidden files) along with permission and ownership details

#### `mkdir <path_to_new_directory>`
* What does it do?
  * Create a new directory
* Examples
  * `mkdir new-dir-name` - Make a new directory in current directory
  * `mkdir /full/path/to/new/dir` - Make a new directory at the specified location
  * `mkdir relative/path/to/new/dir`

#### `pwd`
* What does it do?
  * Print full path to the current directory

#### `rm <path_to_file>`
* What does it do?
  * Remove a file
  * **Note** - `rm` permanently deletes files without sending them to trash first, so be careful!
* Examples
  * `rm /full/path/to/file` - Remove specified file
  * `rm relative/path/to/file`
  * `rm ../../../relative/path/to/file`
  * `rm -r /full/path/to/dir` - Remove specified directory and all of its contents (files and subdirectories)
  * `rm -r relative/path/to/dir`

#### `touch <path_to_file>`
* What does it do?
  * Create a new file
* Examples
  * `touch new-file-name` - Create a new file in current directory
  * `touch /full/path/to/new/file` - Create a new file at the specified location
  * `touch relative/path/to/new/file`
  * `touch ../../../relative/path/to/new/file`

## Other Concepts and Commans
* `grep`
* `echo`
* `which`
* Subshells and `$()`
* Permissions and `chmod`
* Ownership and `chown`
* Parameter expansion
* Shell variables
* Conditionals and `test`
* `$PATH`
* `~/.bash_profile`
* `source`
* `export`
* `PYTHONPATH`
