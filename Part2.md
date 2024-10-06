# Create files via the command line

![image: how to make a file in terminal](https://i.ytimg.com/vi/BEZXXAIsQNA/hq720.jpg?sqp=-oaymwEhCK4FEIIDSFryq4qpAxMIARUAAAAAGAElAADIQj0AgKJD&rs=AOn4CLChcKeTrto9uJJ09b274ucbOGwA8w)

Setting up folders is cool, but a folder without any contents is as useful as a box with nothing in it!

Now that you're familiar with creating folders via the command line, It is time to fill those folders with files.

We will stick with the format of the last chapter, meaning we will show **one example of creating files without code** in them and **the other with code**. This way, even if you are not a programmer already, you can have an appreciation of why folders and files are useful for programmers as well!

> Maybe the code-based example will even motivate you to take your next steps as a coder!

## Creating files

### Non-code example

In the last chapter, you created a folder structure for **school coursework**. This folder was called second semester. As a little exercise in the previous chapter, you also created folders inside the second semester folder for each course (art history, biology, etc).

As you can imagine, **different courses** will require **different kinds of files** inside. For example, a humanities class like art history might require an end of term paper. This file is likely to be a text file. 🎨 Maybe the biology class will require research and findings from this semester! This file is likely to be a spreadsheet. 🐢

**You can create all types of files from the command line itself.**

This is much faster than creating the file individually via different applications like Microsoft Excel or a word processor and running "Save As."

Let's first work with the art history example. If you use the command `cd` to move into the "Art history" directory, you can then use a command called `touch` to create a file for our end-of-term paper.

**Touch** is a fairly creepy sounding command, but here's what it does:

- tells your system to look for a certain file

- If the file not already exist, your system will create that file for you.

In this case, let's create a file called `term-paper.txt` .

> Be sure to check that you are creating the file in the "Art history" directory. If you're ever unsure of exactly where you are, remember that you can run the `pwd` command anytime to show you the folder that you're currently in.

The command will look like this:

```
touch term-paper.txt
```

It's as simple as that! Now if you look back in Finder, you will be able to see that this file has been created inside your "Art history" folder. It is currently empty, but you can **open** it at anytime from Terminal to edit the contents as you normally would:

```
open term-paper.txt
```

Now it's time to create a second file. This second file will be in the Biology folder. This means we have to **change directories** to the Biology folder!

You can put into practice changing directories to move up one level. Two dots represent the parent directory of the directory where you are currently, so you can `cd ..` to move up one level in your folder structure.

```
cd ..
```

> Two dots (..) always symbolize a parent directory! This means if I'm in a folder, but I want to move up to the folder that **contains** my current folder, I run `cd ..` regardless of what that folder's name is.

At this point, you would be back in the "Second semester" directory.

Now, you can type `cd Biology` to move into the Biology directory. From here, you can write the same touch command with the name of the file you want to create and the file extension.

```
touch research-findings.csv
```

> CSV is simply a file extension for structured data sets. Don't worry if you're not familiar with it already.

Here is what the whole series of commands looks like:

![Run the open command to open a file](https://user.oc-static.com/upload/2017/10/05/15072284858977_opencommand.png)
Run the open command to open a file

Notice that upon running `open research-findings.csv`, the file opens automatically in Microsoft Excel. Terminal is smart enough to know which application should open which file type. 👍

![The file opens in the correct application!](https://user.oc-static.com/upload/2017/10/05/15072285055939_spreadsheet.png)
The file opens in the correct application automatically!

> You can even see the **contents** of a file from the command line using a command called `cat` plus the filename. For example `cat ~/Documents/Art\ history/term-paper.txt` would show the text contents of my art history term paper.

### Code example

In the previous chapter, you saw how to create a basic folder structure for a static website. There was a CSS folder and a folder for images.

However, both are empty. Let's add a file!

Once in the `project` directory, you will create an empty **HTML file**. This file is typically the most fundamental page of any basic code project. HTML files are where the **structure of the webpage** will live and where you define paragraphs or headers, where you want elements like navigation bars, or how text should be formatted.

> No worries if you don't know HTML yet! This is just a demo to give you a peek into a programmer workflow. 😅

Run `touch` plus the name of the file -- `index.html` -- to create it:

```
touch index.html
```

Now, by typing `ls`, you can see the project contains a CSS folder, a folder for images, and a file called `index.html`. We'll come back to this file in a second.

![Creating an index.html file](https://user.oc-static.com/upload/2017/10/05/15072283402186_indexhtml.png)
Creating an index.html file

Let's `cd` into the `css` directory and create another file here. This new file will have a different extension than the others we've created so far: it won't be .txt, nor .csv. nor .html. It will be .css because it will hold CSS code!

```
cd css
```

```
touch main.css
```

> I'm naming these files according to standard HTML and CSS traditions. You can read more about the [HTML5 boilerplate here](https://html5boilerplate.com/).

I can even open the HTML file in my browser to preview my file contents:

```
open index.html
```

You now have a sense of how versatile and streamlined file creation is from the command line. It's much faster than creating files individually via different applications like Word.

You just have to know the **name of your file** and the **extension** you want, and you can save yourself a lot of time and totally avoid the Save As process within different applications.

> _In the next chapter, you'll see how to move around and copy some of this content you've created._
