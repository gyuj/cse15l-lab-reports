# Lab Report 4

## Part 1
---

// Task : In the DocSearchServer.java file, change the name of the *start* parameter and its uses to *base*.

// My lab group came up with the shortest sequences of keys to press to complete this task with vim commands that were less than 30 keystrokes. 

The steps are below

1. First, there are two things to check. Make sure that you are in visual mode, if not, `esc`
out to exit insert mode. Then make sure that your cursor is at the top of the file, so that we may start off with finding the *first* instance of the word "start" that we want to replace. If not at the top, hold the key `option` and click your cursor to the top. 

2. There is a manual way to search for every instance of the word "start" in our file and replacing it every time, but to shorten the keystrokes, we will feed our commands to search and replacing with another word into one line of command. The command is below. 

```
:%s/start/base/gc
```
![lab04-firstcommand](lab04-firstcomm.png)

3. Above, as soon as the command is typed in, the first instance of "start" is already highlighted to be edited. 
As soon as you press 'enter', a green prompt is shown on the bottom, instructing us to input 'y' or 'n' for replacing each instace of the "start" word with "base". 

![green-prompt](lab04-green-prompt.png)

4. Now, we just need to input `y` three times to replace the first three instances of the word, and a `n` for the last instance, because we only want the replacement to happen within the class FileHelpers. 

// Changes made to the file in sequence as `y` and `n` is inputed by the user is shown in the screenshots below. 

> We can see that the first *start* has been replaced.
![first-y](lab04-first-y.png)

> We can see that the second *start* has been replaced.
![second-y](lab04-second-y.png)

> We can see that the third *start* has been replaced. 
![third-y](lab04-third-y.png)

> After prompting `n`, the last *start* has not been replaced as intended, and is kept. Since there are no more *start* instances to replace, the command has terminated and there is a summary note of the changes and edits to the file that has been just made. 
![fourth-n](lab04-fourth-n.png)

> In summary, the total keystrokes has been 28; actual typed in command is below.

> :%s/start/base/gc<Enter>yyyn



## Part 2
---

// Task : Running the docsearch file in Visual Studio Code locally andthen running `scp` to copy the file over remotely to run the tests took me 2 min and 44 seconds. My computer is also slow when logging into my ssh account itself, so it may have taken longer to scp over the file from my local server. 

When running the test on my docsearch file remotely *after* I had done`ssh` into my remote server already, it only took 2 minutes and 3 seconds. Now that I was familiar with vim already and also had practiced editing the file in vim in the least keystrokes, it did not take too long of a time. 

// Questions to Answer
1. Which of these two styles would you prefer using if you had to work on a program that you were running remotely, and why?
> If it was something I was running remotely, I would personally `ssh` first andthen make the edits through vim. I feel pretty comfortable quickly navigating through the file, and I'm also able to quicky scroll and `option` click to find the spot for editing, which may have taken a longer time if I had only used jklh. Also, I know which commands to type in vim if I make a mistake, and having the *undo* option is very useful and provides a safe place for editing in vim. This would allow me to safely and comfortably edit files remotely using vim without messing anything up to lose my progress. 


2. What about the project or task might factor into your decision one way or another? (If nothing would affect your decision, say so and why!)
> However, if the task or project was something that was complicated and was comprised of multiple edits to the file, then it would be better to edit on Visual Code, and make all the changes conveniently, and then push all together. 
