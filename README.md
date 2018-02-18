# Mini-Shell
Python shell of file handling
MINI-SHELL 
A shell is an ordinary program that reads commands from the user and executes them, and is the primary user interface to traditional Unix-like systems. The fact that the shell is a user program, and not a part of the kernel, illustrates the power of the system call interface. 
A process consists of user-space memory (instructions, data, and stack) and per-process state private to the kernel. Processes can be time-shared; available CPUs are transparently switched among the set of processes waiting to execute. When a process is not executing, its CPU registers are saved, and restored when the process is next run. The kernel associates a process identifier, or pid, with each process. 
A process may create a new process using the fork system call. Fork creates a new process, called the child process, with exactly the same memory contents as the calling process, called the parent process. Fork returns in both the parent and the child. In the parent, fork returns the child’s pid; in the child it returns zero. 
The exit system call causes the process to stop executing and to release resources such as memory and open files. The wait system call returns the pid of the current process; if none of the caller’s children has exited, wait waits for one to do so. 
The exec system call replaces the calling process’s memory with a new memory image loaded from a file stored in the file system. Exec takes two arguments: the name of the file containing the executable and an array of string arguments. When exec succeeds, it doesn’t return to the calling program; instead the instructions loaded from the file start executing at the entry point declared in the ELF header. If exec returns, it’s always because of an error. 

The OS module in Python provides a way of using operating system dependent
functionality.  The functions that the OS module provides allows you to interface 
with the  underlying operating system that Python is running on – be that 
Windows, Mac or Linux. 
OS functions
import os

Executing a shell command
os.system()    

Get the users environment 
os.environ()   

#Returns the current working directory.
os.getcwd()   

Return the real group id of the current process.
os.getgid()       

Return the current process’s user id.
os.getuid()    

Returns the real process ID of the current process.
os.getpid()     

Set the current numeric umask and return the previous umask.
os.umask(mask)   

Return information identifying the current operating system.
os.uname()     

Change the root directory of the current process to path.
os.chroot(path)   

Return a list of the entries in the directory given by path.
os.listdir(path) 

Create a directory named path with numeric mode mode.
os.mkdir(path)    

Recursive directory creation function.
os.makedirs(path)  

Remove (delete) the file path.
os.remove(path)    

Remove directories recursively.
os.removedirs(path) 

Rename the file or directory src to dst.
os.rename(src, dst)  

Remove (delete) the directory path.
os.rmdir(path)    
