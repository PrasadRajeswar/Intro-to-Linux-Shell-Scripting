# Intro-to-Linux-Shell-Scripting  
A shell script is simply a plain text file that contains a series of commands and shell statements when a shell script is executed it in turn executes the commands listed in the script that starts at the very top and executes the commands on each line one line at a time until the end of the file. Executing a shell script produces the exact same result as you typing in each line directly into the terminal. This means any work you can do on the command line can be automated by a shell script.    
## Text-Editor   
We need a text editor to edit and execute the shell script. If you have already installed your favorite text editor good to go! if not, then either you can install gvim, gedit or any other text editor you want. Else, you can start with `vim` or `nano` text editor. some distro comes with nano inbuilt while in some machine, we need to install it.
To install the nano text editor, execute the following command in the terminal.    

For RedHat based system,    
`sudo yum install -y nano`     
For Debian based system,     
`sudo apt-get install -y nano`    

In this repo, we will be using `nano` text editor to write and execute our shell script.   
At first we open a file in nano text editor. To do so, give-   
`nano day1.sh`   
`.sh` is the extension for the script file. However, unlike the other file formats extension is not necessary. Rather the permission to execute the file is of the top most priority. To check the read, write & executable status of the file give, `ls -l` in the terminal.   
This should return,   
`-rw-r--r-- 1 dell dell 0 Apr 16 15:14 day1.sh`
Let's breakdown the above-
`- denotes that it's a text file.   
d- denotes that it's a directory.
r- read permission
w- write permission
`   
So, we can see that our file `day1.sh` doesn't have execute permission. To make the file executable give,   
`chmod +x day1.sh
or
chmod +xr day1.sh`   
where, `chmod` stands for change of mode and `+x` is the file execute permission. after this, again run `ls -l` on the terminal.   
Now the output comes as-   
`-rwxr-xr-x 1 dell dell 0 Apr 16 15:17 day1.sh
where, x is executable permission`

NOTE- In the command, `-rwxr-xr-x`   
1. `-` denotes its a text file.
2. First three `rwx` denotes permission given to the owner of the file.
3. Next three `r-x` denotes permission given to the group of the file.
4. Last three `r-x` denotes permisison given to everyone else in the system.
To execute the file, you need to have read and execute permisison of that file.
Since now we have execute permisison, it's time to execute the file. But, before that, let's add some content in the file `day1.sh` so that we can see them executing. To do so, open the file through `nano day1.sh` command and add the following to it.
`#!/bin/bash
echo "You don't need to be great to start something but, you need to start to be great.`
Then, `ctrl+o` to save and `enter` to confirm the file name and exit. Furthur, give the `./day1.sh` to execute the file. after executing, the output shall be following-
`You don't need to be great to start something but, you need to start to be great.`
Have you noticed, we wrote `#!/bin/bash` in the top line in our file `day1.sh`. What does that mean???
The `#!` means `shebang` It determines what path the program will be executing in the file.
the `echo` however is a builtin command to print the content in the file.   












