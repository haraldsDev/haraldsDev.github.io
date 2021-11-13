---
layout: default
---

## Command line course outline

This was my first (programming) course at Helsinki University. I was not sure what (how much) to expect. It turned out to be more intense than I had expected before – about 5 times more reading and watching material for a week. At some point I just get used to it, and was spending ~ 1,5 - 2 hours for it every day. At the end I feel more comfortable with many command line tools, and if something doesn't work I just try different approach.

The original Mouse image, just to check, if the image works:

![alt mouse should appear here][mouse]

[mouse]: https://assets.petco.com/petco/image/upload/f_auto,q_auto/135143-Center-1 "Logo Title Text 2"

<br/><br/>

## Week 1: Introduction to Command Line Environments

After the first week in the command line, you are able to:
+ list the contents of your current directory,
+ change your current directory, 
+ download contents from the internet, 
+ display a text file using less,
+ create and remove files and directories,
+ copy, rename and move files,
+ open and edit a file in text editor

<br/><br/>

```
 ls -d */
```

there is a nice command **`ls -d */`** which lists only directories in the current directory.

<br/><br/>

**Reflection**: Emacs felt quite unwieldy. Otherwise, this week gave a lot of useful commands.

<br/><br/>

## Week 2: Navigating a UNIX System

Main goals for the Week2:
+ You are able to copy, move and delete a directory.
+ You have visited the root directory of your system. 
+ You know how to compress a file and a directory using gzip and tar.
+ You know how to find out and change the read and write permissions for a file.
+ You can find the PID of a process and kill it.
+ You're able to run commands in the background.
+ You know how to form a remote connection to a server.
+ You can to copy files to and from a server using scp.

<br/><br/>

An example of very usefule code how to copy an entire directory from remote server to local machine:
```
scp -r matuliha@puhti.csc.fi:/users/matuliha/lda-t302/exercise2 
~/Desktop/H/Helsinki/Helsinki-Courses-2021/LD-T302-Computational-Morphology
```
**scp** stands for *copying*, the **-r** flag stands for *recursively*, and it is followed by two destination paths: source and target.

<br/><br/>

**Reflection**: In this week I learned about **scp** command, and also started to use **emacs** – a command line editor. I also learned **gzip** and **tar** commands.

<br/><br/>

**Here is a nice picture from File-System** tutorial, which shows what every specific folder is for:
![alt there should be a picture of File-System][preg]

[preg]: https://github.com/haraldsDev/haraldsDev.github.io/master/assets/img/File-System-Picture-as-jpeg.jpeg "Logo Title Text 2"


In case the previous picture didn't show, here is a Reference logo from Markdown tutorial, which for some reason works:

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"


<!-- ![ alt reference logo][ref_logo]
[ref_logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2" -->


<!-- 
[logo]: https://github.com/haraldsDev/haraldsDev.github.io/blob/master/assets/img/File-System-Picture.png "A picture of File System on Unix" -->

<!-- [logo]: /Users/Haralds/src/cmd-website/haraldsDev.github.io/assets/img/File-System-Picture.png "A picture of File System on Unix" -->

<!-- /Users/Haralds/src/cmd-website/haraldsDev.github.io/cmdline_course.md -->

<br/><br/>

## Week 3: Basic Corpus Processing

The learning contents of Week3 were:

+ You know the difference between the ASCII, Latin-1 and utf-8 encoding systems
+ You can convert a text file from Latin-1 to utf-8 encoding
+ You can convert Windows text files into UNIX text files and vice versa
+ You know how to print the first N lines and last N lines of a text file
+ You know how to count the number of lines, words and characters in a text file
+ You know how to transform all upper case characters in a text file into lower case characters
+ You can sort the lines in a file into alphabetical and numerical order
+ You can remove duplicate lines from a sorted text file
+ You know how to find all lines in a text file which start with an upper case character
+ You can search for patterns in files
+ You can cut columns from formatted text files
+ You can paste columns into formatted text files
+ You can save results of your operations as a new file (using >)

<br/><br/>

Here is a code for transforming lowercase **a** to uppercase **A** throughout the file katinka_rabe.utf-8.txt:

```
cat katinka_rabe.utf-8.txt | tr "a" "A"
```

<br/><br/>

**Reflection**: ASCII, Latin-1 and utf-8 was a very useful topic, it helped to calm down about why files are not working sometimes. Also line-ending differences between Unix and Windows was useful - I had previously encountered Git complaining about line-endings, and now I understand better what it is.

<br/><br/>

## Week 4: Advanced Corpus Processing

Learning outcomes of Week4:

+ You can delete lines from a file using sed
+ You can find and replace patterns from a file using sed
+ You can use regular expressions with sed
+ You understand how commands can be piped in UNIX using pipe `|` operator
+ You know how to generate a frequency list from a text file
+ You know how to generate sentence per line format from a text file
+ You know how to transform a text file into a list of word n-grams

<br/><br/>

An example of a Table, by showing frequency list of 4 most frequent words from "Life of a bee"  text:

Frequency | Word
--- | --- 
4602 | the
2559 | of
1845 | and
1663 | to 

<br/><br/>

**Reflection**: This was a good practice in **sed** and with **grep**. I had some previous experience with regular expressions, so this was not so hard for me, although the subtle differences between **grep** and **egrep**, and between **bash** and **zsh** – it made me nervous. The conclusion was that it is better to stick to one tool / environment where you know 100% how every command will perform.

<br/><br/>

## Week 5: Scripting and Configuration Files

The learning outcomes of week5 were:

+ You can write simple scripts
+ You know how to access command line parameters in scripts
+ You know what the if statement does
+ You understand command substitution
+ You can see the values of existing environment variables using echo
+ You can change their values of existing environment variables and define new ones using export
+ You can make these settings permanent by placing them into your .bashrc / .bash_profile file.
+ You can use the .bashrc / .bash_profile files to create a pleasant working environment for yourself! This can include a nice prompt or shortcuts for commands you use often.

<br/><br/>

**Reflection**: This week I enjoyed, because I got more experience with **.bash** files. I also did a lot of reading on subtle differences between different files. At the end I felt more comfortable to write some commands in **.bash** file to customize the experience. Also, during the course I switched from **zsh** which was the default interpreter to **bash** as there were subtle, annoying differences to **zsh** which made it hard to follow the materials - as everything had to be re-done a bit differently.
However, after the course I felt comfortable enough, to locate my **.zshrc** file and copy contents from it to **.bash_profile** file - because I had done some downloads and I had relevant commands written on **.zshrc** file.

<br/><br/>

Here is an example of a bash file I have:

```
#!/bin/bash

adj=$1
#echo $adj

start="${adj%?}"
lastchar="${adj: -1}"

case $lastchar in
   e)
        echo ${start}er
        ;;
   y)
       echo ${start}ier
       ;;
   *)
       echo ${adj}er
       ;;
esac
```

Here we see the characteristic syntax of Bash:
+ `#` stands for commented out line, unless followed by `!` which marks the beginning of the bash file
+ bash allows variables assignment, like `adj=$1`. When referring to a variable we have to precede it with a `$`.
+ notice also the syntax of `case` statement – in order to exit it, we have to use `esac` – a common convention in Bash language: to spell backwards the keyword to exit some block of code.

<br/><br/>

## Week 6: Installing and Running Programs

Goals of week6:

+ You can give commands as the root user, preferably using sudo
+ You can install software in your system using apt-get or brew
+ You can install python packages using pip
+ You can search for apt-get, brew or pip packages online or using the tools' search functionalities, and follow instructions on how to install them (OK, this is too general - but at least you have some idea on how)
+ You can create a python virtual environment for yourself, and install packages in that environment
+ You can write a Makefile and run it

<br/><br/>

**Reflection**: This was a very intense week. If after section on bash scripts I felt that it is the upper limit - **Makefile** pushed the limit further. I experimented with **sudo**, found out the differences between **pip** and **pip3**, learned more about **brew**. I still find annoying the differences in syntax of bash scripts, Makefiles, sed etc. etc. – it just makes hard to use them. But I also got the point, that they have evolved so historically (not on purpose to be different), and also I really appreciated the benefits they can give in automation and optimization of routine procedures!

<br/><br/>

Here we have an example Makefile from Week6:

```
BOOKS=alice christmas_carol dracula frankenstein heart_of_darkness life_of_bee moby_dick modest_propsal pride_and_prejudice tale_of_two_cities ulysses

FREQLISTS=$(BOOKS:%=results/%.freq.txt)
SENTEDBOOKS=$(BOOKS:%=results/%.sent.txt)
#BIGFILE=$(BOOKs:%= >>)

all: $(FREQLISTS) $(SENTEDBOOKS)

clean:
        rm -f results/* data/*no_md.txt

%.no_md.txt: %.txt
        python3 src/remove_gutenberg_metadata.py $< $@

results/%.freq.txt: data/%.no_md.txt 
        src/freqlist.sh $< $@

results/%.sent.txt: data/%.no_md.txt
        src/sent_per_line.sh $< $@
```

Here we have the characteristic syntax of Makefile:
+ **BOOKS=** — to define variables
+ `FREQLISTS=$(BOOKS:%=results/%.freq.txt)` – defining **FREQLISTS** as an operation on **BOOKS**
+ a command to process all text files `%.txt` and save the result in a similarly named file prefixed by `no_md`:
```
%.no_md.txt: %.txt
        python3 src/remove_gutenberg_metadata.py $< $@
```
<br/><br/>

## Week 7: Version Control

The goals of Week7:

+ You understand what is, and why we should use version control
+ You commit internally to use version control whenever you are developing a large-ish project. Opening a github repository for the projects you undertake at is also good practice for your CV, since you can share your Github profile.
+ You have Git installed and ready-to-use in your system.
+ You can set up a repository in Github.
+ You can clone this repository in your local computer.
+ You can add files to your local repository, commit these changes, and push the changes to your global repository in Github.
+ You can undo the changes you made by reverting to a previous commit version.
+ You understand why we use branches. You can create branches and switch between them.
+ You can merge a branch into your master branch.

<br/><br/>

**Reflection**: I had previous experience with git, so this was not so hard. I was nice to learn about GitHub pages - it seemed really an easy way to publish something on web. I learned some new things about relationship between **local** and **remote** repos – or perhaps, it has changed and evolved in the last years, and I just didn't know that.

<br/><br/>

A code example – how to do git merge:

+ `git checkout master` – so that we are on a master branch - INTO which we want to merge our changes
+ `git pull origin master` – a good practice to first pull the changes from remote repo.
+ `git merge calc-divide` – we merge **calc-divide** locally into **master** branch.
+ `git push origin master` – followed by pushing local master to remote master.

<br/><br/>

## Final Week: Jekyll and Gihub Pages

Main topics and takeaways from the Final Week:

+ setting up Jekyll, installing everything
+ customizing my GitHub repo for GitHub pages
+ learning about templates and experimenting with adding bits and pieces of data.

<br/><br/>

Here is an example code how to solve build error related to GemFile:

```
gem "kramdown-parser-gfm"
```

<br/><br/>

**Reflection**: All in all I felt relieved, that it was so (comparatively) easy to set up everything with Jekyll, the local server also worked really well - I have had some previous experience wiht local servers in web development, where you had to refresh manually. Although, I still have some reservations about using all different kind of programming languages - like **Ruby** for this project – I feel that project looks *messy* with all different file types in the Root folder. It intuitively seems *unclean* and *unscientific* way how to work - if you  don't really know what every file is doing, and you just hop around changing some bits in the existing files. However, I'm learning to accept this part of *programming* life. : )


