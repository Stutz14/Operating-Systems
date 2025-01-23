# Operating-Systems
Operating System Fundamentals
In this assignment, you will have a parent process that will create children processes to perform tasks and
will collect the output from these children processes. There are three tasks that should be performed:
• Read the input file that contains Linux shell commands. Parent process will read that.
• Execute the Linux shell commands read from the input file and execute them one by one. A child
process will be created to execute these commands and the output will be returned by the child
process in the form of string using anonymous pipe.
• The parent process will write the output of the command(s) to the screen using the given function.
• The following flow chart describes the flow of the program.
 Description
Write a C/C++ program that includes the code for following tasks. Write all the code in single file:
1. Write the parent program as per the description in the “Synopsis”. The parent program must use
fork system call to create children process(es) when required.
2. Read the sample input file, sample_in.txt. The name of the file must be given to the main/parent
process through command line arguments. 
a) This file contains one shell command per line.
b) Since the file is created in Windows environment, line terminator is ‘\r\n’.
3. Store the commands in a dynamically allocated array.
4. Execute the commands one by one with the help of a child process:
a) Use a suitable version of exec system call to execute shell commands.
b) The child process must write the output of the command to an anonymous pipe but doesn’t
display it to the screen. The parent process will read the command output from the pipe
and and will display it to the screen.
c) You may use only one child process by doing fork once to execute all the commands or
fork again and again.
d) The parent process must use the provided output function, writeOutput(), to write the
output to the screen. Invoke the output function iteratively, once for each command.
Warning: If you will not use this function to display the output then your outcome
will not match with our outcome, and you will be awarded zero.
5. The other implementation details are on your discretion, and you are free to explore.
6. In order to test your code, use the sample_in.txt and compare the output of your program for
this input file with the content of sample_out.txt. However, keep in mind that due to the nature
of the commands, the output is specific to the content of the directory in which you run your
program. Hence, verify the output of commands by running them directly on Linux shell.
