# Some Linux Commands
---

## 1) Directory
---

### Commands create a new directory :

Command : mkdir dir : This will create a directory name dir.

suppose i have two directory name dir1 and dir2. I am currently present in dir1 and i want to make a file dir3 under dir2, then

command : mkdir ../dir2/dir3

### To list the files present in your directory :

Command : ls

* ls -a : list all files including hidden files.

* ls -l : listing, show permission, edits dates, etc.

### Commands to Change directory :

*cd dir : To move inside a subdirectory. Here dir is the subdirectory.

*cd ~ : To change directory to the home directory. 

*cd : This works same as cd ~.

*cd / : To change directory to the root directory.

*cd .. :  To move to the parent directory of current directory

* ls -1 | wc –l : Count the number of directories in your current directory.

* Suppose i want to move from dir1 to dir2

 Command : cd ../dir2/

### To get the Current Working Directory :

command : pwd

### To recursively list all the directories you have created :

command : ls –R

## 2) Files
---

### To copy, delete, move, rename of files 

* cp file1 file2 : make a copy of file1 named file2

* rm myfile : remove myfile (delete it permanently)

* rm * : remove all files in current directory

* rm -i * : interactive removal - ask yes/no for each file

* mv /home/Dir1/file1 /home/Dir2 : to file1 from dir1 to dir 2

* mv B1.txt A.txt : To rename a file from B1.txt to A.txt

* cat myfile : show contents of myfile

* more myfile : show contents of myfile one screen at a time

* head myfile : show the top 10 lines of myfile

* head –n 4 f1.txt : Prints the first 4 lines of the file

* head –c 4 f1.txt : Prints the first 6 bytes from the file specified.

* tail -3 f1.txt : Prints the last 4 lines of the file

* tail –c -11 f1.txt : Prints the last 11 bytes from the file specified.

* sort f1.txt : will rearrange the lines in a text file so that they are sorted, numerically and alphabetically

* sort –r f1.txt : To perform a reverse-order sorting

* sort –n num.txt : To sort a list of numbers in a file.

* sort –k3 det.txt :To sort the table on the basis of 3rd column.

* sort –k 2n det.txt : 	To sort the table on the basis of 1st column.

### Comaparing Files 

* cmp file1.txt file2.txt : It compares two files of any type and writes the results to the standard output. By default, cmp is silent if the files are the same; if theydiffer, the byte and line number at which the first difference occurred is reported.

* cmp –b file1.txt file2.txt : displays the differing bytes in the output.

* cmp -i 5 file1.txt file2.txt : To skip a particular number of initial bytes from both the files and then after skipping it compares the files.

* comm doc.txt doc1.txt : It compares two sorted files line by line. With no options, comm produces three-column output. Column one contains lines unique to file1, column two contains lines unique to file2, and column three contains lines common to both files.

* comm –nocheck -order doc.txt doc1.txt : To find the common from non sorted  input files.

* diff doc.txt doc1.txt : It tells which lines of one file have to be changed to make two files identical

* diff –c doc.txt doc1.txt : To view differences in context mode.

* grep –i –c “Dog” animals.txt: Find the total number of lines contains the word ‘Dog’ in animals.txt.

* –i –v –c “Dog” animals.txt : find the total number of lines does not contain the word ‘Dog’ in
animals.txt.

* grep –i –c "Cat$"" animals.txt : Display the lines in animals.txt that end with the word 'cat'.

* grep –l “cat” * : To display the files containing "cat".

### Changing permision of a file

* Chmod 600 A.txt : To have read and write permission for the owner, but keep the
file private from others. 


## 3) Date & Time
---

* Cal –A3 : Display 3 months from now.

* Cal -M : Display Monday as the first day.

* cal –d 1752-09 : Display September of 1752.

* cal –d 2015-03-09 –A3 : Display 3 months from the date 9 th March 2015

* date +"Today’s Day : %u"  : Display day of this week.

* date +"Week number : %W" : Display week number of the year.

* date +"%d %B %Y" : Display Date on this format - 12 th April 2020.

* date +"%d %b’%y" : Display Date on this format - 12 th Jan'20.

* date +"%d/%b/%y" : Display Date on this format – 05/07/98.

* date : Display current date with hour minute second

* date +"%r" : Display the current time in 12-hour format.

* date –d "2018-09-22" +"%A" : With a user-specified date, display only the day of the week (e.g. Tuesday).

## 4) Numericals
---

* echo ‘sqrt(4)’|bc : To find the square root of 4.

* a=5 b=6 z=15

  Total= ‘expr $a* $b + $z / $a’

  echo $Total  : To perform ((5*6)+(15/5))

* echo "a=10;a^=2;a" | bc : To print 10^2=100.

* $expr 12 \* 2 : to multiply two numbers.

* sum=`expr $x + $y` : to add two user input numbers.

## 5) To check existance of a file 
---

* test –e det.txt && echo " Exists" || echo "does not exists" : Determine if a file exists or not using test command.

* check=det.txt
  [ -e $check ] echo " Exists" || echo "does not exists" : Determine if a file exists or not without using test command.

## 6)Compare two strings using and without using test command.
---

read a 

read b

* test [$a==$b] && echo "True" || echo "False" : To compare two strings using test command.

* [[ $a==$b ]] echo "True" || echo "False" : o compare two strings without using test command.
