# code2pdf
Convert code to pdf with LaTeX and Minted. Created with the intention for printing code.

## About
code2pdf is a bash script that adds contents from code files to a single latex file. The latex file is then compiled with latexmk.

### Options
The options for the bash script are the file names. One keyword argument is the language of the code, which is set with the `-l` flag.

For example: `./code2pdf file1.py file2.py -l python`

There also options in the latex file. The variable is used to create page breaks. This helps seperate files by pages. For example, when printing the pdf with double sided, it may not be desirable for a new file to start on the back side of page. If the new file should start on a new piece of paper, then set `\pages{2}`. If the modulo of the page number of the beginning of a file and `\pages` is not zero, then a new page will be created.
