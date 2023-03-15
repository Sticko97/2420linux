---
tags: Linux, Virtualization, Vagrant, Introductions
---

# Week 1

## Learning Outcomes and Topics
This week:
- Introductions
- Course Outline
- What is Linux
- Set up a Linux VM
	- Overview of some of the tools that we will be using this term

Next week:
- Review of several commands used to navigate and find things in the command line
	- ls
	- cd
	- pwd
	- grep
	- find
- Getting help in the command line
	- using manules with the `man` utility
	- using `help` for bash builtins


## Introductions

**About me**
- I started using a Linux distribution in the late 90s, [Slackware](http://www.slackware.com/)  
- Most of my professional work has involved a Linux operating system.  
	- I have primarily worked in System Administration and DevOps fields.  
- In my free time I like to try out new Linux distros and other open source software.  
- Over the years I have contributed to a number of open source projects.  
- I also enjoy some of the usual nerdy things:  
	- Sci-Fi  
	- Comics  
- When I am not doing something related to the above I am probably climbing  

**About You**
- Do you have a favorite programming language or tool or technology related to the program?  
	- If so what is it and why?  
- Do you have any previous experience using a Linux OS or a BSD OS? (other than 1420)  
- On a scale of 1 - 10 how comfortable are you working in the command line?  
- Outside of your school work what do you like to do? What is a primary hobby of yours?   

## Course Outline


**Evaluation Criteria**

| Criteria | % | Comments |
|----------|---|----------|
| Quizzes | 10 | |
| Labs | 20 | |
| Assignments | 20 | 2x 10% each |
| Midterm Exam | 25 | |
| Final Exam | 25 | |

**Office Hours**

Tuesday   11:30-12:30  
Thursday  09:00-10:00  
Friday    09:00-10:00  
==Please schedule at least 24 hours in advance via email or discord==

**Course Notes**

Course notes are distributed as plain text Markdown files.

The intention is that you will clone the repo and every week do a `git pull` to get the current week's notes. Once you have the notes, open them up and add your own notes to them as you work through the material.

If you are unfamiliar with Markdown, it is a simple markup language (think simplified HTML).  
You can write Markdown in any plain text editor (vim, vscode...) or one of the many note-taking apps that use Markdown. A lot of apps that you are already using probably use Markdown. For example, Notion and discord both use Markdown. 

Markdown is also used for a lot of technical documentation, most of the README files you have seen on GitHub are written in Markdown. 

[Markdown syntax cheat sheet](https://www.markdownguide.org/cheat-sheet/)

**Late Submissions**

Late submissions will be accepted up until 4 days.  
10% will be deducted per day.  
The first day begins the moment you are late. ie if an assignment is due at 23:30 and you submit at 23:31 you are a day late.

The entire course outline is available [here](https://www.bcit.ca/outlines/20231089212/)

## Some of the tools that we will be using this term

### VirtualBox 
[VirtualBox](https://www.virtualbox.org/) is a relatively easy to use virtual machine manager that is available for Linux, MacOS and Windows.

### Vagrant
[Vagrant](https://www.vagrantup.com/) Is a tool that can be used to create VM configuration in plain text files.
This means that you save your setup for a VM in a text file on GitLab for example and you can quickly recreate a new VM using this file.

### Ubuntu
[Ubuntu](https://ubuntu.com/) is a popular Linux distro used on servers, and desktops.  
Ubuntu comes in two official versions:  
- LTS 22.04  
- 22.10  

Generally, you would use the LTS(long term support) version for production work. Since we aren't going to be creating anything for production, we are going to use the slightly newer 22.10 version.

### Windows Terminal
[Windows Terminal](https://github.com/microsoft/terminal) is already installed if you are using Windows 11. In Windows 10, you can install it from the Microsoft store.
[A video intro to Windows Terminal](https://www.youtube.com/watch?v=2dsnwlnNBzs)

This is obviously only for people using Windows. If you are using BSD, Linux or MacOS you probably already have a decent terminal emulator.

### WSL
[WSL](https://learn.microsoft.com/en-us/windows/wsl/about) Windows Subsystem for Linux is a tool that you can use to run a Linux environment from within Windows. This is a popular tool for developers who use Windows because it gives them easy access to a Linux development environment.

### DigitalOcean
[DigitalOcean](https://www.digitalocean.com/) DigitalOcean is a cloud service provider. We will be using this near the end of the term, so we will come back to it then.

## Before we get started, some useful terminology

**open source**

open source software is software that provides the source code which can be freely used, shared and modified.

Do You think open source software is less secure than closed source software?  
What is your reason for thinking that?

About 90% of most applications are built on open source code.
[Video on 2022 open source stats](https://www.youtube.com/watch?v=g0LYPJitubc)

[open source](https://opensource.org/licenses)

**Free software**

Although Free and open source are not the same thing, they are often related, and are very much related in the context of Linux based operating systems.

> Thus, “free software” is a matter of liberty, not price. To understand the concept, you should think of “free” as in “free speech,” not as in “free beer”.
> [GNU philosophy](https://www.gnu.org/philosophy/free-sw.html)

**System administration, SRE(site reliability engineer) and DevOps**

In as broad a definition as is possible, a system administrator is someone who configures and keeps computer systems running.

A site reliability engineer is someone who works in operations and solves operations problems as if they were software problems.

> DevOps is a modern way to deliver higher quality applications faster - by automating the software delivery lifecycle, and by giving development and operations teams more shared responsibility and more input into each other’s work.

> Like SRE, DevOps makes a business more agile by balancing the need to deliver more applications and changes faster with the need to avoid 'breaking' the production environment. And like SRE, DevOps aims to achieve this balance by establishing an acceptable risk of errors. In fact, SRE and DevOps seem so similar that some experts say they're the same thing - but most see SRE practices as excellent ways to implement DevOps principles. 
> [IBM](https://www.ibm.com/cloud/learn/site-reliability-engineering)

## Virtualization review

> Software called [hypervisors](https://www.redhat.com/en/topics/virtualization/what-is-a-hypervisor) separate the physical resources from the virtual environments—the things that need those resources. Hypervisors can sit on top of an operating system (like on a laptop) or be installed directly onto hardware (like a server), which is how most enterprises virtualize. Hypervisors take your physical resources and divide them up so that virtual environments can use them.  
> Red Hat, What is virtualization


- Is VirtualBox an example of a type 1 or type 2 hypervisor?
- What are some reasons that an individual or organization might use a VM?

![Type 1](../images/type1.webp)

![Type 2](../images/type2.webp)

[Red Hat, What is virtualization](https://www.redhat.com/en/topics/virtualization/what-is-virtualization)

[Short Video on Virtualization](https://www.youtube.com/watch?v=FZR0rG3HKIk)

## What is Linux

- What is Linux?
- What is a Linux distro?
- Who is using Linux and what are they using it for?
	- Why are these people using Linux?
- Who created Linux?
	- Who is maintaining it now?

![Linux Time Line](../images/Linux_Distribution_Timeline_21_10_2021.svg)


**The Linux Kernel**

![The Linux kernel](../images/kernel.jpg)


The kernel has 4 jobs:

1.  **Memory management:** Keep track of how much memory is used to store what, and where
2.  **Process management:** Determine which processes can use the central processing unit (CPU), when, and for how long
3.  **Device drivers:** Act as mediator/interpreter between the hardware and processes
4.  **System calls and security:** Receive requests for service from the processes

**Distros that I use regularly**

[Fedora Silverblue](https://silverblue.fedoraproject.org/)

[openSuse MicroOS](https://microos.opensuse.org/) (I am using this right now)

[Alpine Linux](https://www.alpinelinux.org/)

[OpenBSD](https://www.openbsd.org/) (not Linux, but closer to Linux than MacOS or Windows)

[Red Hat What is the Linux kernel](https://www.redhat.com/en/topics/linux/what-is-the-linux-kernel)  
[IBM, The Linux kernel](https://developer.ibm.com/articles/l-linux-kernel/)


## Reading

Readings should be completed before the start of next weeks class.

Most of the readings will be available on O'Reilly learning. You have access to this through BCIT. In the past, students have used this before in other classes and know how to access readings here. If this is not the case, let me know and I will add instructions here.

This week's readings come from *A Practical Guide to Linux Commands, Editors, and Shell Programming*, Fourth Edition, by Mark Sobell and Matthew Helmke

Chapter 2, *Getting Started*
- [Working from the Command Line](https://learning.oreilly.com/library/view/a-practical-guide/9780134774626/ch02.xhtml#ch02lev1sec4)  
- [`man`: Displays the System Manual](https://learning.oreilly.com/library/view/a-practical-guide/9780134774626/ch02.xhtml#ch02lev2sec5)  

Chapter 3, *The Utilities*
- [Basic Utilities](https://learning.oreilly.com/library/view/a-practical-guide/9780134774626/ch03.xhtml#ch03lev1sec3)  
- [`less` Is `more`: Display a Text File One Screen at a Time](https://learning.oreilly.com/library/view/a-practical-guide/9780134774626/ch03.xhtml#ch03lev1sec4)  
- [Working with Files](https://learning.oreilly.com/library/view/a-practical-guide/9780134774626/ch03.xhtml#ch03lev2sec6)  

---

# Week 2 Jan 16

## Learning Outcomes and Topics

This week:
- explain reasons why you want(need) to use the command line in 2023
- explain how commands are executed in a shell
- learn to use a few commands that will help you navigate in a command line environment
  - cd
  - pwd
  - ls
- learn how to use the `man` utility
- learn how to read man pages
  

Next week:
- The Linux file system
- Finding files with `find` and `grep`
- command line text editors:
  - vi(m)
  - nano
  - helix

## Why are we still using the command line?

The reading from last week (everyone did the reading, right) provides a few good reasons to use the command line in 2023.

- Servers, and other minimal Linux configurations, where a GUI is:
  - unnecessary
  - adds complexity and might introduce additional vulnerability

Personally, I think the best reason to use the command line still is that it is really powerful. 
When you get even a little more comfortable with the command line you will find that you are able to achieve a lot of tasks faster than in a GUI.

One reason for this is that commands are a programming language. 
The shell is a REPL. It is possible to combine commands that generate data, with commands that filter data.

For example, man pages(more them later). 
If I wanted to search for a man page that allows me to change a user's password I could use `man -k password`. 
The information is in there, but it is a lot of data to sort through. So I add a filter with `grep` `man -k password | grep change`. 
This command returns a lot less data. Now I can open the man page, read how to use `passwd` and change a user's password.
All from the same tool!

Working in a text based interface can be tricky at first, and it takes practice. However, it is totally worth it. So stick to it.

## Getting around in the command line

Everyone probably knows the `cd` command. An interesting note about `cd` is that it is a shell built-in. 
Unlike `grep` which is a separate utility, `cd` is actually part of bash. 
You can find out about other shell built-ins with `help` if you want to see help for `cd` `help cd`.

`cd` is change directory, we can use it to change the location we are running commands in. 

*What does `cd ..` do?*

**`ls`**

The `ls` utility lists the contents of your current working directory.

On Linux OSs, and Mac and Windows, "hidden" files are created by starting the file name with a '.'. 
For example ".bashrc". Generally these are hidden so that an average computer user doesn't do anything to them. 
They are generally used to configure software and services on your device. 

You can see the hidden files with `ls -a`.

In addition to showing you a list of files, `ls` can also show you information about those files. 
`ls -l` "-l" is "long listing". This shows you file permissions, ownership, the date the file was last edited and the files size. 
You can combine l and a `ls -ahl`. *What do you think -h does? How could you find out?* 

```
-rw-r--r-- 1 riversng river 1150 Sep 26 19:51 filename
|[-][-][-]-  [------] [---]
| |  |  | |     |       |
| |  |  | |     |       +------------> 7. Group
| |  |  | |     +--------------------> 6. Owner
| |  |  | +--------------------------> 5. Alternate Access Method
| |  |  +----------------------------> 4. Others Permissions
| |  +-------------------------------> 3. Group Permissions
| +----------------------------------> 2. Owner Permissions
+------------------------------------> 1. File Type
```

**Your prompt**

Most of the time when you connect to a remote server, or open a terminal from a desktop you will be in the home directory of the user you are logged in as.

You will likely see something that looks a little like this`username@hostname ~$` (this will be slightly different depending on the operating system that you are using. This little string is your shells prompt. The shells prompt usually provides you with some handy information. 

`username` is your user name, the user who is currently running commands in the shell. You can change users in the shell.

`hostname` the hostname of the machine you are connected to. 

The tilde character `~` is shorthand for the users home directory `~ = /home/vagrant` this is the directory where commands will be run. So if you run the command `mkdir week2` you will be creating a new directory in `/home/vagrant` 

The `$` is commonly used to represent a regular user, but it has no special functionality, some shells use a `%` as the default prompt character.

The `#` is likewise often used to represent root.

The information in your prompt is configurable, you can change it to provide more or less information. We will look at some basic configuration later on.

`pwd` this will print the name of the current working directory, where you are in your file path.

**Important**

“Your home” directory and “the home” directory are not the same thing.

Your home refers to `/home/user-name` 

The home directory is just `/home` this is where all of the users home directories are. Unless you are creating or removing a user you generally don’t run any commands from `/home` 


## A few special characters

We are going to see a lot of "special characters" in the command line. I might start a list in your notes.

The pipe character `|` will "pipe" output from one command into another command. Like filtering the man page search above.

The double ampersand `&&` `sudo apt update && sudo apt upgrade`. 
This command is actually two commands, the second will run only if the first succeeds. If the first returns an error the second command won't run.

`mkdir` this will make a directory `mkdir new-dir` `mkdir -p new-dir/other-new-dir`. *What do you think the second command does?*

## Options, or Flags

These are additional (optional) information that we can pass to a command. 
Some options take arguments, others do not. Options that don't take arguments can be written like this `ls -alh`

## Practice tips

In addition to just trying to use the command line more (try not using your file finder for a day.), try incorporating two new things to your command line skill set every week. 
This week, try these two things:
1. Use tab more to complete commands
2. Try using ctrl + u(delete command entered so far) and ctrl + w(delete a word) instead of backspace when you make a typo.

[keyboard shortcuts](https://www.computerhope.com/ushort.htm)

[Red Hat 10 terminal shortcuts for Linux](https://www.redhat.com/sysadmin/top-10-shortcuts)

## Getting help in the command line.

Earlier you saw `help` however the main tool used to learn more about commands is `man`. Short for manual.

### Pagers

When you open a man page you are opening the manual entry in a pager, `less`. 
A pager, shows you a page of info at a time.
- To find out how to use less press `h`
- To quit press `q`

### reading a man page

| Bold | type this exactly, this is often the command |
| --- | --- |
| [OPTION] | options or flags, ie -a |
| italic or underlined | Replace with appropriate argument |
| -a | -b | Options separated by pipe cannot be used together |
| … | Arguments followed by an ellipses can be repeated |
| <mandatory> | Mandatory argument, usually found in option descriptions |
| {yes, no} | Limited options, only those specified will work |

**Headings of a man page**

Not all of these headings will be in every man page

- **Name:** The name of the command the man page is describing.
- **Synopsis:** A summary of the command and its syntax.
- **Configuration:** Configuration details for a device.
- **Description:** An explanation of what the program does.
- **Options:** A description of the command-line options the command accepts.
- **Exit Status:** Possible exit status values for the command, and what might cause them to be used.
- **Return Value:** If the man page is for a library
routine, this describes the value the library routine can send back to
the function that called that routine.
- **Errors:** A list of the values that might be placed in `errno` [in the event of an error](http://man7.org/linux/man-pages/man3/errno.3.html).
- **Environment:** A list of the environment variables that affect the command or program, and in what way.
- **Files:** A list of the files the command or program uses, such as configuration files.
- **Attributes:** A summary of various attributes of the command.
- **Versions:** Details of the Linux kernel or library
versions where a system call or library function first appeared or
changed significantly from previous versions.
- **Conforming to:** A description of any standards with which the command might comply, such as [POSIX](https://en.wikipedia.org/wiki/POSIX).
- **Notes:** Miscellaneous notes.
- **Bugs:** Known issues.
- **Examples:** One or more examples demonstrating the use of the command.
- **Authors:** The people who wrote or maintain the command.
- **See also:** Recommended reading related to the command or topic.

**Additional Resources**  

[Arch wiki man page](https://wiki.archlinux.org/title/Man_page)

**Bookmark this tool** [explain shell](https://explainshell.com/https://explainshell.com/)
 

## Reading

**Reading Questions**
- How would you describe the Filesystem Hierarchy Standard?
- What is a Pseudo Filesystem
- What is the difference between /usr/bin and /bin
  - What is the historical difference
- Where are system level configuration files
- How do open a new file in Vim
- How do you save a file in Vim
- How do you search for a file in Vim

[Learning Modern Linux Ch 5. Filesystems](https://learning.oreilly.com/library/view/learning-modern-linux/9781098108939/ch05.html)

[Learning vi and Vim editors, 8th ED, Ch 1. Introducing vi and Vim](https://learning.oreilly.com/library/view/learning-the-vi/9781492078791/ch01.html)

---

# Week 3

## Learning Outcomes and Topics

This week:

- Filesystem Hierarchy Standard
- Describe how most Linux directories are structured
- Use `lsblk` and `tree` to learn more about filesystems
- Use vi(m) to edit several files
- Introduction to `find` and `grep` to find files

Next week:

- Permissions and Ownership
- Users and Groups

## Utilities

Last week, we looked at a few utilities to help move around on the filesystem. This week we are going to look at tools to help learn more about the filesystem, tools to find files and tools to edit files. Most of these tools are already installed. The `tree` utility can be installed with the following command. `sudo apt install tree` In a later class, we will talk more about sudo and apt.
DigitalOcean note: When you are the root user you don’t need to use sudo.

## Filesystems

In general, when people talk about a filesystem they might be talking about 2 different, but very closely related things.

A file system or filesystem such as ext4 or btrfs is the underlying data structure used to separate and organize files on your system. There are a number of different types of filesystem, ext4 is a journalling filesystem, btrfs is a copy-on-write filesystem for example. Most of the time, a person using a computer doesn’t need to worry about which filesystem their machine is using (often more than one). 

The command `lsblk --exclude 7 -f` can be used to see how partitions on your Linux machine are formatted, which filesystem they use.

When you are installing a Linux OS, unless you have a good reason to change the filesystem, I recommend installing what the developers have setup as the default.

Resources:

[File systems](https://wiki.archlinux.org/title/File_systems)

[Btrfs](https://wiki.archlinux.org/title/Btrfs)

[Ext4](https://wiki.archlinux.org/title/Ext4)

## Filesystem Hierarchy Standard

The Filesystem Hierarchy Standard, or FHS is a good starting place, although not strictly adhered to. Different Linux distros will differ slightly in where certain things are stored.

[Filesystem Hierarchy Standard](https://refspecs.linuxfoundation.org/FHS_3.0/fhs/index.html)

Are there any directories that contain the same content? 
Why do you think that is?

As we progress through the class you will have more opportunity to explore some of these directories.

When I was learning to use Linux I would cd into a directory and try to find out what some the things inside that directory did.
Don't worry about breaking things, it is just a VM, and most "important" stuff you can't change without sudo.

![fhs](../images/fhs.png)

There’s a man page for this too 😯 `man hier`

The `tree` utility is a little like `ls`,only it shows youthe contents of a directory, as well as subdirectories in a tree. Tree is great for exploring how files are organized.

The `tree` command will print a lot material.

We can narrow down the output with the `-d` and `-L` options. Try this `tree -dL 1`

You can also combine `tree` with `less` and a pipe, like this `tree -dL 2 | less`.

Note on terms:

- I sometimes use command, when I am talking about using a utility, running a command.
- And a utility when I am refering to the program itself.

**Pseudo Filesystems**

Last week I said “In Linux, everything is a file”. An interesting example of this is the `/proc` directory.

The `/proc` directory contains processes and kernel information files.
`/proc` makes use of the virtual file system to allow a user to interact with this data in the same way that you would what we more traditionally think of as a file. For example you can cat the uptime file to see how long your system has been up. 

## Finding Files with `grep` and `find`

`grep` and `find` are utilities that you will use a lot, you have already seen `grep` used to help narrow down the number of items returned when searching for a man page with `man`

Both `grep` and `find` can be used to help you; find files. `grep` searches the content of files, what is in the files and `find` searches for files by name, type, size…

[Red Hat 10 ways to use the Linux find command](https://learning.oreilly.com/library/view/learning-modern-linux/9781098108939/ch04.html)

[Red Hat How to use grep](https://www.redhat.com/sysadmin/how-to-use-grep)

## Command Linux Text Editors

![Vim](../images/vim.png)

Last week, we talked about a couple of reasons that we are still using the command line. Two of those reasons were: Servers don’t need a GUI and the fact that the command line can be really powerful and fast. Command line editors are an extension of both of these.

Sometimes you need to make small edits to a file on a server. You could edit the file locally, copy it to the server, delete the original… You can already see that this won’t always be the most efficient way to work. If you just need to change a line of text, open the file in a command line editor and edit the file.

Some of the things we talked about last week in terms of power and speed are relative, too. Many of the tools that we use on the command line are so great, because they are small, simple tools that can be combined to perform more complex tasks. A text editor is no different. 

## Why Vim

Why should you learn vi and Vim:

1. Vim is everywhere, from servers to key bindings in most other editors.
2. It's scalable. You can use it just to edit config files or it can become your entire writing and coding platform.
3. It's powerful.

Number 1 is the reason that we are interested in vi(m) today. vi really is everywhere, so it is a good idea to know the basics.

### vi, Vim and Neovim

[Vim](https://www.vim.org/)

[Neovim](https://neovim.io/)

### Modal Editing

What is a modal text editor?

The short answer is that it is an editor with different modes 🤔

Each mode has a specific purpose. That is to say, you would switch to that mode to perform certain tasks. 

Why is normal/command mode the default?

How would you describe a modal text editor to someone new to vim?

**vi modes:**
  - **command** mode (this is normal mode in vim)
  - **insert** mode

**vim modes:**

  - **normal** mode (this is the mode that you start vim in by default) escape
    use normal mode for many edits, removing text, changing indentation...
  - **insert** mode (this is basically the only mode other poor vscode has (unless you have the vim
    plugin for vscode)) i
  - **visual** mode use visual mode to make visual selections v
    - visual line mode, select one line at a time shift + v
    - visual block mode, select in blocks ctrl + v

  - **replace** mode replace text. replace mode is like insert but will write over existing text
      with the new character R

  - **command** mode allows you to enter commands that start with a : as well as run shell
    commands `:! mkdir new_dir` will create a new directory in your current working directory
    command mode can also be used for things like search and replace  

Just the basics

What other tool have we used in class with some of the same keybindings?

Provide an example of a keybinding that both tools share?

Vim commands

| Vim Command | Description |
| --- | --- |
| i | Enter Insert mode |
| Esc | Return to Normal mode from other modes  |
| x or Del | Delete a character |
| X | Delete character is backspace mode |
| u | Undo changes |
| Ctrl + r | Redo changes |
| yy | Copy a line |
| dd | Delete a line |
| p | Paste the content of the buffer |
| /<search_term> | Search and then cycle through matches with n and N |
| [[ or gg | Move to the beginning of a file |
| ]] or G | Move to the end of a file |
| :%s/foo/bar/gci | Search and replace all occurrences with confirmation |
| Esc + :w | Save changes |
| Esc + :wq or Esc + ZZ | Save and quit Vim |
| Esc + :q! | Force quit Vim discarding all changes |

## Getting help

Yes, there is a man page for vim `man vim` however vim also has builtin help.
You can access vim's builtin help with `:help`

You can access a specific section in the docs with `:help topic` ie `:help yank` will open documentation on copying in vim.

`:help` will open a split window above your current window. This is just another buffer so you can navigate through it with vim keys you can close it with `:bd` buffer delete.
You can move to a different split with Ctrl+w Arrow-keys for example `ctrl + w down-arrow` will take you to a split below the split you are currently in.

## Movements

How would you move to the top of a document?
How about to the bottom of a document?

One of the promises of Vim is that if you put in the time to learn Vim, you will be able to edit code faster.
I believe this is true (I also don't think you need to use Vim to be a good software developer)
One of the ways that Vim will speed up your workflow is a combination of editing commands and movements.

You already know that `h = left, l = right, j = down and k = up`

But this is just the beginning.

Some of these movements can also be combined with numbers. For example what do you think `2j` will do?

A more extensive Vim cheat sheet

[Vim Cheat Sheet](https://vim.rtorr.com/)

![vim cheat sheet](../images/vimmove.png)

## vim commands are composable

Can you think of a more complex example than 2j? What does it do?

Believe it or not, this simple little `2j` example is an incredibly powerful feature of vim.

Commands in Vim are composable. They form a simple language, and you can combine commands to make more complex commands. Vim commands are a programming interface 🤯

`4dd` and `4dj` will delete the current line and the following 3 lines.

### Verbs

Verbs are the actions we take, and they can be performed on nouns. Here are some examples:

- **`d`**: delete
- **`c`**: change
- **`y`**: yank (copy)
- **`v`**: visually select

### Modifiers

Modifiers are used before nouns to describe the way in which you're going to do something. Some examples:

- **`i`**: inside
- **`a`**: around
- **`NUM`**: number (e.g.: 1, 2, 10)
- **`t`**: searches for something and stops before it
- **`f`**: searches for that thing and lands on it
- **`/`**: find a string (literal or regex)

### Nouns

In English, nouns are objects you do something *to*. With Vim, it's the same. Here are some Vim nouns:

- **`w`**: word
- **`s`**: sentence
- **`)`**: sentence (another way of doing it)
- **`p`**: paragraph
- **`}`**: paragraph (another way of doing it)
- **`t`**: tag (think HTML/XML)
- **`b`**: block (think programming)

From [https://danielmiessler.com/study/vim/#files](https://danielmiessler.com/study/vim/#files)

## finding text

Which key would you use to find the character on a line before another character?

To search for a word in your file, use `/` forward or `?` backward

to move to the next occurrence of a character, use `f` for find ie `fa` will move to the next “a” on a line (if there is an a)

There is also a `:find` command, this is used to find files for editing by their name.

### Some other modal text editors

- **[Helix](https://helix-editor.com/)** This is the editor that I use in class.
- **[Kakoune](http://kakoune.org/)**

## Reading

**Reading Questions**
- How do change a files permissions
- What are the permissions that a user can have
- How many users can own a file
- Can a user belong to more than one group
- Which command can you use to change the ownership of a file?
- What are the three permissions scopes files have (the who)

[Learning Modern Linux, Ch 4, Access Control](https://learning.oreilly.com/library/view/learning-modern-linux/9781098108939/ch04.html)

---

# Week 4

## Learning Outcomes and Topics

**This Week:**

- Look at users, groups, ownership and permissions
- create a new user with `useradd` / `adduser`
- give a new user a password with `passwd`
- add a user to group with `usermod`
- view file ownership and permissions with `ls`
- change file permissions with `chmod`
- change file ownership with `chown`

**Next Week:**

- More on the shell
    - streams
    - processes
    - intro to scripting in bash

## Users, Permissions and Groups

In Week 2 we looked at this🔻 some output from the `ls` command, and what it all means.

```
$ ls -al
total 0
-rw-r--r--  1  mh9  devs  9  Apr 12 11:42  test
^           ^  ^    ^     ^  ^             ^
|           |  |    |     |  |             └──  filename
|           |  |    |     |  └──  last modified date
|           |  |    |     └──  filesize in bytes
|           |  |    └── group the file belongs to
|           |  └──  user the file belongs to
|           └──  number of hard links
└──  file mode (- indicates a regular file) and permissions g/u/o
```

The small amount of text above illustrates the main topics that we are going to talk about today. All three of these things, Users, Permissions and Groups are used as part of a relatively simple access control system. That is to say, Users, Permissions and Groups determine *who* can do *what* with a file.

## Users

We could separate the two types of users into:

- Regular users, humans (this could include root)
- System users, daemons might make use of system user accounts to run services, such as a database.

Every user on the system has a **UID**, user identification. You can view a user's UID with the `id` command.

- UID 0 Is `root`
- UID 1 to 999 Are reserved for system
- users UID 65534Is user `nobody`—
    - used, for example, for mapping remote users to some
      well-known ID, as is the case with [“Network File System”](https://learning.oreilly.com/library/view/learning-modern-linux/9781098108939/ch07.html#nfs)
- UID 1000 to 65533 and 65536 to 4294967294 Are regular users.

**Some important files associated with Users and Groups**

| Purpose | File | Explanation|
| --- | --- | --- |
| User database | /etc/passwd |This stores information about the user(everything but the password is stored here)|
| Group database | /etc/group |     |
| User passwords | /etc/shadow |     | 
| Group passwords | /etc/gshadow |     |

/etc/passwd  
/etc/group




We have looked at the `/etc/passwd` file before, as used in an example to compare man pages and different sections. The passwd file stores data about all the users on a system. Each field is separated by a colon. 

```
root:x:0:0:root:/root:/bin/bash
|    | | | |    |     └──>  The Login Shell
|    | | | |    └──>  The users home directory
|    | | | └──>  users information, generally this is just name
|    | | └──> Group ID (GID)
|    | └──>  User ID (UID)
|    └──>  x indidcates that the user has an encryped password in the shadow file
└──>  The users name
```

**Creating a new user**

There are a few different tools that can be used to create a new regular user on a Linux OS. Today we are going to use the `useradd` command. The reason that we are using `useradd` instead of `adduser`(which is used in the textbook) is because `useradd` is available on most, if not all Linux OSs. 

`adduser` is a little more confusing. Sometimes `adduser` is a perl script, sometimes it is linked to `useradd`. Fedora for example, if you try to open the man page for `adduser` you will see the man page for `useradd`. And sometimes it is not available at all.

So we are going to use `**useradd**`

The `useradd` command can be used to define many attributes of a new user, where their homed directory is, which login shell they use and a password, although you shouldn’t use this for adding a password from the command line. (see the man page for why)

The defaults for some of these values are defined in `/etc/default/useradd`

When a new user is created, the default configuration files in /etc/skel can be added to the new user's home directory. Generally these are bash configuration files, but we could add other default configuration files, like a .vimrc file if we wanted to.

**Giving a new user a password.** 

Earlier I said not to use the password option with `useradd` from the command line, so how do we give a new user a password? With the `passwd` utility.

## Groups

In addition to Users, Linux distros have the concept of Groups. Every user belongs to at least one group, their user group. Users can belong to more than one group.

To see the groups that your user belongs to you can use the `groups` command

Adding a user to a group is one way that you can give a user permissions to perform certain tasks. The most general example of this is adding a user to a group that belongs to sudo. On most Linux distributions, this is ‘wheel’ or ‘sudo’. On Ubuntu it is the sudo group.

Just like regular users, system users have a default group. Adding a regular user to that group allows the regular user to perform certain tasks with that software.

You can add a new regular user to group with the `usermod` command.

`sudo usermod -aG sudo <user-name>`

The `-aG` options are important -a = append, without this the new group will replace your existing groups. -G is a list of groups that you want to add a user to.
replace <user-name> with the user you want to add to the sudo group. For example, if I have a regular user ‘pond’ on the system. `sudo usermod -aG sudo pond`. This will add pond to the sudo group and pond will be able to use sudo.

[Users and groups](https://wiki.archlinux.org/title/Users_and_groups)


## Permissions and ownership

Every file on a Linux OS is owned by one user and one group.  Files also have permissions associated with them. 

Permissions on a file are of three scopes (or three categories of who):

- User
- Group
- Other

And each scope has some combination of three possible permissions:

- Read
- Write
- Execute

When you run the `ls -l` command in directory, you can see the file permissions of each file. 
In the example below, the permissions are:

- User
    - read, write and execute
- Group
    - read and write
- Other
    - read

```
d rwx rw- r--
^ ^   ^   ^
| |   |   └──  other
| |   └──  group
| └──  user
└── file type (d indicates a directory)
```

Permissions have a symbolic representation (rwx) and a numeric representation (0-7)

**Permissions table:**

| Pattern | Effective permission | Decimal representation |
| --- | --- | --- |
| --- | None | 0 |
| --x | Execute | 1 |
| -w- | Write | 2 |
| -wx | Write and execute | 3 |
| r-- | Read | 4 |
| r-x | Read and execute | 5 |
| rw- | Read and write | 6 |
| rwx | Read, write, execute | 7 |

ownership can be changed with the `chown` command.

`sudo chown user:group file` change the user and group that own a file.

`sudo chown user: file` also change user and group that own a file.

`sudo chown user file` change only the user that owns a file.

`sudo chown :group file` change only the group that owns a file.

Remember system users, users that are processes. One reason that you might change the ownership of a file is to give a service permission to write to a file. 

You can change permissions on a file with the `chmod` command. The `chmod` utility can be used with both the symbolic and numeric (sometimes referred to as the octal) method.

The symbolic method uses a combination of values that represent permissions and scope and operations that represent the change you want to make. 

```
- '+' add a permission
- '-' remove a permission
- '=' set a permission explicitly
```

`chmod u+x file` will add execute permissions to the user.

`chmod a+x file` will add execute permissions to the user, group and other

`chmod u+x,g+w,o-r file` will add execute to the user, write to the group and remove read from other.

`chmod u=rw,g=r,o= file` will set the users to read and write, groups to read and other to nothing.

The numeric method is a little more succinct.

`chmod 644 file` will set the user's permissions to read and write and group and other to read. 

[Inodes and the Linux filesystem](https://www.redhat.com/sysadmin/inodes-linux-filesystem)

[Users and groups](https://wiki.archlinux.org/title/Users_and_groups#Permissions_and_ownership)

## Sudo and Root

As mentioned earlier, you can add a user to the sudo group, which on an Ubuntu based OS will allow that user to use the sudo command. This grants a user temporary elevated privileges.

The sudo command has configuration files in `/etc` `sudo.conf` and `sudoers` 

| File | Purpose |
| --- | --- |
| /etc/sudo.conf | Configuration for the sudo command |
| /etc/sudoers | Configuration for who can use sudo |

For example, the sudoers file on my system contains the line `%wheel ALL+(ALL) ALL` Which grants members of the wheel group the ability to do everything with sudo.

Why do we have the sudo command? Why not just use the root user for everything?

[Sudo](https://wiki.archlinux.org/title/Sudo)

## Reading

**Reading Questions:**

- Why should additions to PATH go in .bash_profile?
- What are streams in Linux?
- How do you run a startup file in the current shell?
- When is a PID assigned?
- What is a background process?
- How are commands run by the shell?
- What should the first line of a shell script be?

Read the following sections from [A Practical Guide to Linux Commands, Editors and Shell Programming](https://learning.oreilly.com/library/view/a-practical-guide/9780134774626/ch05.xhtml#ch05) Ch 5:

- Standard Input and Standard Output

[A Practical Guide to Linux Commands, Editors, and Shell Programming, Fourth Edition](https://learning.oreilly.com/library/view/a-practical-guide/9780134774626/ch05.xhtml#ch05)

Read the following sections from [A Practical Guide to Linux Commands, Editors and Shell Programming](https://learning.oreilly.com/library/view/a-practical-guide/9780134774626/ch08.xhtml#ch08) Ch 8:

- Startup Files
- Processes
- Processing the Command Line

[A Practical Guide to Linux Commands, Editors, and Shell Programming, Fourth Edition](https://learning.oreilly.com/library/view/a-practical-guide/9780134774626/ch08.xhtml#ch08)

Read the following sections from [Learning Modern Linux](https://learning.oreilly.com/library/view/learning-modern-linux/9781098108939/ch03.html) Ch 3:

- Scripting

[Learning Modern Linux](https://learning.oreilly.com/library/view/learning-modern-linux/9781098108939/ch03.html#scripting)

---

# Week 5 2420

## Learning Outcomes and Topics

This Week:

- Discuss how the shell executes a command
- Edit the .bashrc to create an alias
- Use the `ps` utility to view running processes
- Use redirects to redirect streams
- use a shebang in a shell script to specify an interpreter from within a file
- Write hello world in bash
- Write a shell script to create a new user on a server

Next Week:

- Midterm Exam

After the Midterm:

- Scripting
- Assignment 1
- WSL
- DigitalOcean

## Executing commands in the shell

We have been running commands in the shell since week 1. This week, we are going to dive a little deeper into what actually happens when we run a command.

The following is a brief description of the shell’s operation when it
reads and executes a command.  Basically, the shell does the
following:

1. Reads its input from a file (see [Shell Scripts](https://www.gnu.org/software/bash/manual/html_node/Shell-Scripts.html)), from a string
supplied as an argument to the `-c`  invocation option
(see [Invoking Bash](https://www.gnu.org/software/bash/manual/html_node/Invoking-Bash.html)), or from the user’s terminal.
2. Breaks the input into words and operators, obeying the quoting rules
described in [Quoting](https://www.gnu.org/software/bash/manual/html_node/Quoting.html). These tokens are separated by
`metacharacters`. Alias expansion is performed by this step
(see [Aliases](https://www.gnu.org/software/bash/manual/html_node/Aliases.html)).
3. Parses the tokens into simple and compound commands
(see [Shell Commands](https://www.gnu.org/software/bash/manual/html_node/Shell-Commands.html)).
4. Performs the various shell expansions (see [Shell Expansions](https://www.gnu.org/software/bash/manual/html_node/Shell-Expansions.html)), breaking
the expanded tokens into lists of filenames (see [Filename Expansion](https://www.gnu.org/software/bash/manual/html_node/Filename-Expansion.html))
and commands and arguments.
5. Performs any necessary redirections (see [Redirections](https://www.gnu.org/software/bash/manual/html_node/Redirections.html)) and removes
the redirection operators and their operands from the argument list.
6. Executes the command (see [Executing Commands](https://www.gnu.org/software/bash/manual/html_node/Executing-Commands.html)).
7. Optionally waits for the command to complete and collects its exit
status (see [Exit Status](https://www.gnu.org/software/bash/manual/html_node/Exit-Status.html)).

[Shell Operation (Bash Reference Manual)](https://www.gnu.org/software/bash/manual/html_node/Shell-Operation.html)

## A process is a running instance of a program

When you run a command, like `ls` or `git push` you are starting a new process.

## Child and parent processes

> Like the file structure, the process structure is hierarchical, with parents, children, and a *root.*
 A parent process *forks* (or *spawns* ) a child process, which in turn can fork other processes. The term *fork* indicates that, as with a fork in the road, one process turns into two. Initially the two forks are identical except that one is identified as the parent and one as the child. The operating system routine, or *system call,* that creates a new process is named **fork**().--A Practical Guide to Linux Commands, Editors, and Shell Programming, Fourth Edition
> 

When you start a new process, that process is a child process of the command that started it.

Using the above example, `git push` that would look like this:

- bash
    - git push

A child process of a command might start another process, which would be a child of the second process.

- bash
    - vim
        - grep

## Using the `ps` and `pstree` utilitities

There are a number of commands that we can use to help us visualize this. The `ps` command is a good place to start.

The `ps` command by itself will show you something like this🔻

```bash
PID TTY          TIME CMD
   6869 ?        00:00:00 bash
  10797 ?        00:00:00 ps
```

This is just the ps command itself and the parent process, bash. Try running the command `ps --forest` This will help you visualize the relationship between these commands.

If you want to see all of the running processes, there are two options

The BSD version:

- ps -aux
    - The `a` option tells `ps` to display the
    processes of all users. Only the processes that not associated with a
    terminal and processes of group leaders are not shown.
    - `u` stands for a user-oriented format that provides detailed information about the processes.
    - The `x` option instructs `ps` to list the processes without a controlling terminal. Those are mainly processes that are started on boot time and running in the background.

And the Unix version:

- ps -ef
    - The `e` option instructs `ps` to display all processes.
    - The `f` stands full-format listing, which provides detailed information about the processes.

The `ps` command also includes a formatting option, `-o` which lets you select the output.

`ps -eo comm,rss` will show you the command and ram used by a process.

You can combine this with a command like `grep` to filter the output 

`ps -eo comm,rss | grep ssh`

`pstree` is similar, only as the name might suggest it shows things in a tree like structure by default.

`pstree -p` show PIDs

## Streams and redirects

There are three streams in Linux shells

- 0: stdin
- 1: stdout
- 2: stderr

- 0 representing standard in are commands be written to the shell, usually these come from a keyboard
- 1 representing standard out are messages printed to the shell. The output of commands
- 2 representing standard error are error messages printed to the shell.

Sometimes you want to redirect streams from one location to another.

One of the most common examples of this is writing the output of a command to a file.

What is the difference between the two examples below?

```bash
ls -l > file
ls -l >> file
```

We can also redirect from a file to a command. 

Imagine I have a file containing names, and I want to sort them alphabetically.

```
Louise
Akiyo
Hannah
Jernej
```

Save the above in a file named ‘names’ and run this command `sort < names` 

Now try this `sort < names > sorted-names` This command will created a new file with the names in alphabetical order.

We can also redirect error messages, a common use case for this is to not show error message.

For example, `find /usr -name ls` I know this is going to include some Permission denied errors. I can redirect those errors to /dev/null (this is a file that doesn’t hold any values, so everything written to /dev/null is disgarded) `find /usr -name ls 2>/dev/null` 

[Redirections (Bash Reference Manual)](https://www.gnu.org/software/bash/manual/html_node/Redirections.html)

[How to manipulate files with shell redirection and pipelines in Linux](https://www.redhat.com/sysadmin/linux-shell-redirection-pipelining)

## Shell configuration files

Shell configuration files, or startup files, allow a user to customize their shell.

| System Wide | Personal | sourced |
| --- | --- | --- |
| /etc/profile | $HOME/.bash_profile | login |
| /etc/bashrc | $HOME/.bashrc | interactive |

There is also a $HOME/.bash_history file, this contains your command history. And a $HOME/.bash_logout.  

### Configuring your shell

There are a lot of things that you can do to configure your working environment by editing your .profile/.bash_profile and .bashrc files.

You can add a new directory to your path. I have the following in my .bash_profile, which adds the directory where programs written in rust are stored. This includes my text editor [Helix](https://helix-editor.com/)

```bash
if [ -d $HOME/.cargo/bin ]; then
	PATH="$HOME/.cargo/bin:$PATH"
fi
```

Why should the above be in .profile and not .bashrc?

You can add shortcuts or change the default behaviour of commands with aliases and functions.

```bash
# aliases
alias ls="ls --color=auto --group-directories-first"

#functions

# create a new directory and enter it
mkd() {
  mkdir -p "$1" && cd "$1"
}
```

You can configure the look of your prompt to add information about projects that you are working on. Things like Git status, the version of python a project uses…

**Reading shell configuration files**

After changing your shell configuration files, you need to source them so that the changes are applied. There are two common ways to do this when you are using the bash shell.

```bash
source ~/.profile             # Uses the builtin "source" command
. ~/.bash_profile             # Uses a dot
```

[Bash Startup Files (Bash Reference Manual)](https://www.gnu.org/software/bash/manual/html_node/Bash-Startup-Files.html)

## Intro to shell scripting

### The shebang

The shebang is the first line of a shell script, it tells the shell which interpreter to use when the script is executed. Another way to think of this is instead of running python scripts like `python main.py` you could just do `main.py` Instead of you specifying the interpreter in the command you are specifying the interpreter in the file.

There are two ways that we can write a shebang:

using an absolute path

```bash
#!/bin/bash
printf "hello world\n"
```

using the env utility

```python
#!/usr/bin/env python3
print("hello world")
```

- The shebang isn’t just for bash, you can use it to specify any interpreter.
- The shebang **must** be the first line in a file. In Bash and Python hashes ‘#’ represent a comment, so on subsequent lines this will be a comment, instead of a shebang.

### Hello World in Bash

> The only way to learn a new programming language is by writing programs in it. The first program to write is the same for all languages:  *print the words `hello world`*
 -- Brian Kernighan and Dennis Ritchie, *The C Programming Language*.
> 

To get started, created a new ‘Documents’ directory with a new ‘week5’ directory inside of it.

`mkdir -p Documents/week5` and cd into the new week5 directory.

Save the code below into a new file “hw” and make it executable `chmod u+x hw`

Now run the file like this `./hw` You need to include the `./` because this file is not in your path, so you need to provide a path. `./` is the relative path to the file, if you are in the same directory as the hw file.

```bash
#!/bin/bash
#: Title       : hw
#: Date        : Oct 20 2022
#: Author      : Nathan McNinch
#: Version     : 1.0
#: Description : print Hello, World!
#: Options     : None

printf "%s\n" "Hello, World!"
```

### Hello <variable>

Let’s change the above example so that we can pass a name to our script when we run it and say hello to that person.

```bash
#!/bin/bash
#: Title       : hw
#: Date        : Oct 20 2022
#: Author      : Nathan McNinch
#: Version     : 1.0
#: Description : print Hello, World!
#: Options     : None

NAME=$1

printf "%s\n" "Hello, ${NAME}!"
```

**Variables**

Variables can be declared in bash like this: 🔻

```bash
ANIMAL=cat
```

Notice how there is no white space between the variable name “ANIMAL” and variable value “cat”.

Why do you think this is?

Using uppercase is a convention, but not required. 

**Positional parameters**

`$1` is a “positional parameter”  These access arguments passed into the script when you run it.

If we save the code below into a new file, “print-params”  make that file executable and run it like this `./print-params apple two` What is printed? What is $0?

```bash
#!/bin/bash

echo $0 $1 $2
```

| Special Variable | Description |
| --- | --- |
| $0 | The name of the bash script. |
| $1, $2...$n | The bash script arguments. |
| $$ | The process id of the current shell. |
| $# | The total number of arguments passed to the script. |
| $@ | The value of all the arguments passed to the script. |
| $? | The exit status of the last executed command. |
| $! | The process id of the last executed command. |

[Bash Variables (Bash Reference Manual)](https://www.gnu.org/software/bash/manual/html_node/Bash-Variables.html)

[Bash Reference Manual](https://www.gnu.org/software/bash/manual/html_node/index.html#SEC_Contents)

The Google Bash style guide. 

[styleguide](https://google.github.io/styleguide/shellguide.html)

## Midterm Exam Notes

**Exam Time** 

2 hours

**Exam Breakdown**

- Quiz 20%
- Lab 80%

**What should you study**

Everything. Anything that has appeared in the notes, readings… could be on the midterm.

**How should you study**

- Review your notes
- Make up quiz questions based on the labs and quiz each other. (you can do this online too)
- Review the readings
- Review the labs (the lab component will be similar to a class lab
    - If you missed a lab question, don’t feel like you fully understand something, ask questions.
- I will provide you with a sample quiz (at least one of these questions will be on the exam)

**What do you need**

- A VM running Ubuntu 22.10
    - Vagrant or DigitalOcean, unless you have discussed it with me first, and I have approved your plan C (this is just to limit troubleshooting for multiple operating systems/virtualization tools/…)
    - You may want to have a backup VM. In the event that something goes wrong, (it probably won’t).
- A pen

**Good luck!**
