# 0x16. C - Simple Shell
## Project done in teams of 2 people (Authors: Oyewale Olayiwola, Okeke Omolola)
## :open_book: Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:
* Who designed and implemented the original Unix operating system
* Who wrote the first version of the UNIX shell
* Who invented the B programming language (the direct predecessor to the C programming language)
* Who is Ken Thompson
* How does a shell work
* What is a pid and a ppid
* How to manipulate the environment of the current process
* What is the difference between a function and a system call
* How to create processes
* What are the three prototypes of main
* How does the shell use the PATH to find the programs
* How to execute another program with the execve system call
* How to suspend the execution of a process until one of its children terminates
* What is EOF / “end-of-file”?
## Compilation
Your shell will be compiled this way:
```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
```
## Testing
Your shell should work like this in interactive mode:
```
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
```
But also in non-interactive mode:
```
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$
```
## Tasks
### 0. Betty would be proud
* Write a beautiful code that passes the Betty checks
### 1. Simple shell 0.1
Write a UNIX command line interpreter.
* Usage: simple_shell
### 2. Simple shell 0.2
Simple shell 0.1 +
* Handle command lines with arguments
### 3. Simple shell 0.3
Simple shell 0.2 +
* Handle the PATH
* fork must not be called if the command doesn’t exist
### 4. Simple shell 0.4
Simple shell 0.3 +
* Implement the exit built-in, that exits the shell
* Usage: exit
* You don’t have to handle any argument to the built-in exit
### 5. Simple shell 1.0
Simple shell 0.4 +
* Implement the env built-in, that prints the current environment
### 6. Simple shell 0.1.1
Simple shell 0.1 +
* Write your own getline function
* Use a buffer to read many chars at once and call the least possible the read system call
* You will need to use static variables
* You are not allowed to use getline
### 7. Simple shell 0.2.1
Simple shell 0.2 +
* You are not allowed to use strtok
### 8. Simple shell 0.4.1
Simple shell 0.4 +
* handle arguments for the built-in exit
* Usage: exit status, where status is an integer used to exit the shell
### 9. setenv, unsetenv
Simple shell 1.0 +
* Implement the ``` setenv```  and ``` unsetenv ``` builtin commands
### 10. cd
Simple shell 1.0 +
* Implement the builtin command ''' cd''':
### 11. ;
Simple shell 1.0 +
* Handle the commands separator ``` ;```
### 12. && and ||
Simple shell 1.0 +
* Handle the ``` &&``` and ``` ||``` shell logical operators
### 13. alias
Simple shell 1.0 +
* Implement the ``` alias``` builtin command
### 14. Variables
Simple shell 1.0 +
* Handle variables replacement
* Handle the ``` $?``` variable
* Handle the ``` $$``` variable
### 15. Comments
Simple shell 1.0 +
* Handle comments (``` #```)
### 16. File as input
Simple shell 1.0 +
* Usage: ``` simple_shell [filename]```
## :green_book: Authors

* **Oyewale Olayiwola** - [@OyewaleOlayiwola](https://github.com/olayiwolaA/simple_shell)

* **Okeke Omolola** - [@OkekeOmolola](https://github.com/Montego-arch)

