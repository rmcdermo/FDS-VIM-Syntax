# FDS-VIM-Syntax
Syntax file for the VIM text Editor for Fire Dynamics Simulator Input files. 

Script requires grep to be installed.

usage:
 1) clone a copy of the Git Repository:
$git clone https://github.com/firemodels/fds.git
 2) show the list of tags to get the latest stable release:
 	$cd fds
 	$git tag
 	FDS0
 	FDS6.5.3
 	FDS6.6.0
 	FDS6.7.0
 	...
 3) checkout the latest stable release
 	$git checkout 'FDS6.7.0'
 4) switch to the Source dir, then run the script:
 fds_make_syn.pl 
 The script will find all files with the NAMELIST keyword and and parses all the lines: NAMELIST ....
 to get all the syntax keywords

outputs fds.vim
Place the fds.vim file in the $HOME/vimfiles/syntax folder
add the line:
	au BufNewFile,BufRead *.fds	setf fds
To the filetype.vim file
