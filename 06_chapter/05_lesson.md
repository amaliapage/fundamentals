**WDI Fundamentals Unit 6**

---

##Navigating the Command Line

We can perform actions using the command line by **entering commands**. There is a command to perform virtually any action you can imagine on your computer!

There are commands to open an application, create new files, copy files from one place to another, and a lot more.

Let's start typing commands together.  In your open Terminal window, type `hello?` and press enter:

```
$ hello?
```

Your terminal should respond rudely:

```
-bash: hello?: command not found
```

This is the way your computer tells you that it did not understand the command that you typed in. Remember, we have left the GUI world behind us, so we will no longer have pretty warning messages and alert boxes. Do not worry! In
due time, as we grow comfortable in this new environment, even these cryptic messages will be just as beautiful as any warning box you'll ever see.

Try typing this into your terminal:

```
$ Where am I?
```

Again, a rude response:

```
-bash: Where: command not found
```

Great. We've established that our command line doesn't understand plain English. We will have to use special words to make up our commands. Let's try this one:

```
$ pwd
```

Whoa! It looks like our computer understood that one! It replied with a message like:

```
/Users/corneliusfinch
```

(Note: On your machine, you should have seen `corneliusfinch` replaced with your username!)

If you're following along in **Git Bash on Windows**, this should look similar but slightly different:
```
/c/Users/corneliusfinch
```


What did we just do?

The command `pwd` stands for "Print Working Directory".

This command is used when we want the command line to tell us what folder (or directory) of our computer we are currently in.

Just like the Finder on a mac, your command line interface (CLI) places you in a particular folder
of your computer. `pwd` tells you where you currently are in your filesystem. Usually, when you open the Terminal application, you start off in your "home folder", which is the one that shares the name of your username on your computer.

If we were using Finder, we'd be able to see what files and folders are present in this folder. In a CLI however, if we want to see what files and folders exist in the current location, we need to ask for that with another command.

Let's find out what files are in the folder that we're in.

```
$ ls
```

Lo and behold, the contents of the folder you are in:

```
Applications       Desktop          Documents
Downloads          Library          Movies
Music              Pictures         Public
```

(Note: Again, on your machine, since you may have different files and folders, you may see a additional files and folders when you enter `ls`!)

If you're following along in **Git Bash on Windows**, it's alright if the files and folders that are listed out look a little different, but you should still see similar folders such as `Desktop`, `Documents`, and `Downloads`.

The `ls` command, which loosely stands for "list", lists the contents of a folder.

It looks like there are some folders in here. Let's find out what's inside our `Documents` folder. In order to do so, let's first navigate to the Documents folder.

```
$ cd Documents
```

We have now navigated to the Documents folder.

The `cd` command, which stands for "change directory", is used to navigate to a particular folder on your computer.

This is equivalent to double-clicking the Documents folder in Finder to "go
inside it". We can check that we're in the right place by using `pwd`.

```
$ pwd
/Users/corneliusfinch/Documents
```

Excellent! Now let's find out what's in here, using `ls`.

```
$ ls
funny_cat_picture.jpg
office_stuff
world_domination_checklist.txt
```

(Note: Again, your machine means you will probably see different files and folders!)

In our example, it looks like the `Documents` folder contains a JPG file of a funny cat, a folder
full of "office stuff", and a text file that supposedly contains a checklist for
world domination. Your `Documents` folder probably contains something different.

Now that we've investigated our `Documents` folder, let's go back up to our home folder. Since the home folder contains the `Documents` folder, we can say that the home folder is the "parent directory" of the `Documents` folder.

```
$ cd ..
```

> `..` (two periods, or "dot-dot") is how we say to our command line "parent directory".

Many commands consist of three parts: the command, followed by flags (aka options), and finally, arguments.

```
$ command -flag -otheroption
```

As the name implies, flags set options to tell the command how to do what it's about to do. There may be zero or more options. Options usually start with one or two dashes. Usually one dash is for a short one letter abbreviation, while two dashes is for long name for the option.

[More information on command-line options](http://catb.org/esr/writings/taoup/html/ch10s05.html#id2948149)

For example:

```
$ ls -a
```

Will list *all* files in a directory, which includes hidden files (files whose name begins with a `.`).

```
$ cd Downloads
```

Calls the command `cd` to change directory. It is provided the option of where to navigate to.



---

[Give it a try!](07_exercise.md)
