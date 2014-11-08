xplus-rename
============

A Javascript file to work in conjunction with the Mastercam addon X+ Setup Sheet. This does not work with the Excel setup sheet and tool list.

## About the script ##

### **What does this file do?** ###

Once you define your new column names, X+ will use those names whenever you create a setup sheet or tool list.

### **What *doesn't* this file do?** ###

This file does not add any extra functionality to X+ Setup Sheet and Tool List. It simply changes the name that appears at the top of each column.

## How to use it ##

1) Unzip and place this file in the .../public/documents/X+ folder with the rest of the X+ files. You may have to rename this file, but we'll get to that in a few minutes.

### Rename the .js file to match your configuration name. ###

2) Maybe you have a different configuration file for each machine? No problem! For each of your different configuration files, name a copy of the .js file by the same name. Your configuration file names can be found here.

![](images/sheet-file-name.png)
![](images/tl-file-name.png)

In the above examples, your .js files would be named default_xss.js and default_tl.js. 

### Change the column names ###

3) Open the .js file with a text editor like Notepad. Do not use a word processor like MS Word. To change the column names of your X+ Setup Sheet, edit 'Your text here' that corresponds to the default column name. Be sure that your text is wrapped in single quotes after you make any edits.

4) Remove the "//" comment marker from the beginning of every line of code that you edited. If you ever want to undo your change, add "//" to the beginning of the line of code that you want to undo. Save your file after making any changes.

### Example: ###

Say, instead of 'Comment', you want it to say 'Operation Comment'. Find the line of code that has the existing name in the first set of single quotes and edit the 'Your text here' on that same line in the second set of single quotes. (This script contains every column option available in X+ Setup Sheet and Tool List.) So this line:
`//colNames[i].innerHTML = colNames[i].innerHTML.replace('Comment', 'Your text here');`

should be changed to this:

`colNames[i].innerHTML = colNames[i].innerHTML.replace('Comment', 'Operation Comment');`

![](images/before-and-after.png)

### Notes: ###

If you use Internet Explorer as your browser, you may have to accept the use of this script and "allow blocked content" when you see the popup. This script has been tested in Firefox, Chrome, and IE 10.

