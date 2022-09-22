Files:
- simpsh.c: C file that implements a simple shell program on the linux terminal.

- Makefile: makefile that compiles the simpsh.c upon typing make in the linux terminal.

- README.txt: you are reading this text file.


Authors: Taylor Thomas, Vaiden Logan
- delegation:
Mostly worked in unison in designing, programming, and debugging the c file; we specialized in the following areas:
Taylor worked on taking in input, parsing the command, and deciding based on the tokens in the command which command was being input; Vaiden worked on keeping track of variables using setenv, allowing user to execute files + infrom outfrom, and chdir functionality.

About our program:
Our program runs a while loop, prompting the user to enter a command on the command line through
 stdin, until it detects that the user wants to "quit" via the command. Upon entering a command,
 the command line string is taken from stdin using fgets, and fed into a scanner function,
 which uses strtok to split the command into parsable tokens in an array. This array is
 passed into a parser function which analyzes that tokens to determine what the command was
 typed by the user. 
 
 Issues: All of the functions work for the most part, but there are some edge cases that aren't solved. Also, there's a small issue with IO
 redirection. for doing both infrom: and outto:, they must be in that order. While you can do both infrom and outto, you can also do only infrom or outto.
