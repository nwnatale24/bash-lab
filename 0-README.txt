BASH SHELL SCRIPT LAB EXERCISES

There are four shell scripts in this folder.  None is complete.
Working with your group, finish them all.  Be sure to put everyone's
name in the comment block at the top.


1) fullname

This script should ask for a username, and then print out that
person's full name.

For example, if the user exists:

   elvis> fullname
   Enter username: edison13

   Full name for edison13 is 'Annie Edison'.
   elvis>

   elvis> fullname
   Enter username: testing

   No account 'testing'.

To get the information, you can use this command:

   getent passwd USERNAME.

If it exits with zero (remember return status is in $?) and returns a
string, then it found that user.
If it exits with a return code of 2, that means the user does not exist.


2) addstudent

This script takes two arguments, a username and a file.  If the file
does not exist, is not a regular file, or cannot be read and written,
the script should give an error and quit.

The username should be added to the file, in alphabetical order among
the other names.

For example, the file 'students.txt' in this folder has these names:

    barnes5
    bennett4
    changb66
    edison13
    hawthor9
    lambert2
    nadira11
    perryb2
    winger23

If the command 'addstudent kimann81 students.txt' is run, the file
should then be:

    barnes5
    bennett4
    changb66
    edison13
    hawthor9
    kimann81
    lambert2
    nadira11
    perryb2
    winger23

The old file should be saved with the '.backup' at the end.
So in this example, the original 'students.txt' would still be
available as 'students.txt.backup'.



3) findempties

This script takes an optional argument, which is the name of a folder.
(If no folder is named, use the current working directory.)

It should print out a list of all regular files in the directory which
are empty.

(In this folder, 'EmptyFile' is the only one.)



4) checkfiles

This script takes two arguments, a text file and a folder.

It should report an error if the file does not exist, is not a regular
file, or is not readable.

It should report an error if the folder does not exist, is not a folder,
or is not readable.

The text file will have one filename per line.

The script should go through the filenames (remember a for-in loop
can get its list of words from any source, such as a using a command
substition to cat out a file), and print out names of files which are
on the list but not in the folder.

The command './checkfiles CF-list.txt DirTest' should print:

   Checking folder DirTest against file list CF-list.txt
   Missing files:
      c
      
   

