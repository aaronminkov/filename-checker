For poornames, I designed a program that is split into two different functions:
validateNamesBasic and validateNamesRecursive.

Another function that I created to use as a utility is containsElement.

The validateNamesBasic function begins by defining several variables/arrays
and then proceeds to check if the directory argument is readable.

Then, I ensure that the directory has a trailing forward slash.

After that, I find the filenames of the files stored within the directory
and store that in a local variable "sor".

I use a for loop to read through all of the filenames ("fn") in the given
directory, and then confirm that the name matches each of the 4 rules
mandated by the assignment instructions. If one of these instructions
isn't matched, the variable "valid" is set to false.

Then, I have a for loop that checks if the currently selected filename
is a duplicate with different capitalization.

Finally, I handle printing out the names of the invalid directories/
filenames.


The validateNamesRecursive function simply gets the directory name,
calls validateNamesBasic with that directory, then sifts through the
directory's files with a for loop, calling validateNamesRecursive once
again if a filename is in fact a directory.


The code at the bottom of poornames is in fact what is performed first.
It analyzes the provided arguments and decides whether the input given
by the user is valid for the program to run. If not, various errors
are printed depending on what error is found.
