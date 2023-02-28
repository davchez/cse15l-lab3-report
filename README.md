# CSE 15L Winter 2023: Lab Report 3

## grep: Git Bash Command report

### Word search: grep -E -w "(substring)"

#### Example A
![Image](labreplacement.png)

[Additional grep documentation on -E -w](https://www.cyberciti.biz/faq/grep-in-bash/#:~:text=How%20do%20I%20use,display%20those%20line%20on%20screen).  grep -E -w was used to find all instances of a substring in a given text file.  For Example A, the substring "Oahu" was searched for in the specific text file HandRHawaii.txt.  Produced from the search was each line that had an instance of the substring in the file of interest, wherein the output was redirected to a file called "grep-results.txt".
  
#### Example B
![Image](labreplacement2.png)
  
[Additional grep documentation on -E -w](https://www.cyberciti.biz/faq/grep-in-bash/#:~:text=How%20do%20I%20use,display%20those%20line%20on%20screen).  grep -E -w was used to find all instances of a substring in a given text file.  For Example B, the substring "Lake District" was searched for in the specific text file HandRLakeDistrict.txt.  Produced from the search was each line that had an instance of the substring in the file of interest, wherein the output was redirected to a file called "grep-results.txt".

<br>

### Recursive search: grep -R "(substring)" (directory)
  
#### Example C
![Image](screenshot4.jpg)
  
[Additional grep documentation on -R](https://www.cyberciti.biz/faq/grep-in-bash/#:~:text=How%20do%20I%20use,display%20those%20line%20on%20screen). The -R extension to the grep command employs a recursive search through the contents of every single file contained within the written_2/ directory.  For Example C, the very-specific substring "Bailando con el Diablo" was recursively searched for in all files in written_2/.  As seen in the terminal, the output returned the two files in written_2/ and the specific lines which the substring was contained/mentioned.

#### Example D
![Image](screenshot5.jpg)

[Additional grep documentation on -R](https://www.cyberciti.biz/faq/grep-in-bash/#:~:text=How%20do%20I%20use,display%20those%20line%20on%20screen).  For Example D, the substring "Italy" was recursively searched for in all files in written_2/.  As seen in the terminal, the output returned a large amount of files which had lines containing the substring "Italy".  On the left side is the title of the file which contained the substring "Italy"; on the right side of the title is the specific string containing "Italy".  

<br>

### Simplifying the results: grep -l "(substring") (directory)
  
#### Example E
![Image](screenshot6.jpg)

[Additional grep documentation on -l](https://www.cyberciti.biz/faq/grep-in-bash/#:~:text=How%20do%20I%20use,display%20those%20line%20on%20screen).  The -l extension to the grep command allows for a simplification of the results produced by any grep search.  In Example D, we used the -r extension to recursively search for every file containing at least one instance of the substring "Italy"; however, the terminal was flooded with information that is ultimately unnecessary for finding the title of the file containing an instance of a substring, as it also returned the sentence in which it first appeared.  In this Example E, the -l extension removes the clutter, only returning the title of the files which contain at least one instance of "Italy".  Here, it is much more clear how many and what files contain "Italy" in its contents.
  
#### Example F
![Image](screenshot7.jpg)
  
[Additional grep documentation on -l](https://www.cyberciti.biz/faq/grep-in-bash/#:~:text=How%20do%20I%20use,display%20those%20line%20on%20screen).  The -l extension to the grep command allows for a simplification of the results produced by any grep search.  This Example F employs the same -R -l combination as Example E, just using a more specific substring to return two files containing the instance(s) of "The United States".  For smaller and more niche results like this, it might be redundant to use the -l extension for so few files.  However, it still produces the exact first instance of the substring: so it may prove to be useful in the end for certain uses.

<br>

### Deep recursive search: grep -Rw "(substring)" (directory)
  
#### Example G
![Image](screenshot8.jpg)
  
[Additional grep documentation on -Rw](https://www.cyberciti.biz/faq/grep-in-bash/#:~:text=How%20do%20I%20use,display%20those%20line%20on%20screen).  The -Rw extension to the grep command is an even deeper recursive search for a certain substring.  Not only does it return the files which contain the lines with the searched substring, it returns every single instance of the substring throughout the entire directory.  For example, if one file has more than one instance of the substring "Italy", it will return the title of that file twice, but appended to the right will be the two separate line instances in which the substring appeared.  
  
#### Example H
![Image](screenshot9.jpg)
![Image](screenshot10.jpg)
  
[Additional grep documentation on -Rw](https://www.cyberciti.biz/faq/grep-in-bash/#:~:text=How%20do%20I%20use,display%20those%20line%20on%20screen).  Just to utilize every single grep command extension mentioned in this lab report, the -Rw extension is supported by the following extensions: -l and >.  For Example H, -l simplified the results of -Rw by only returning the titles of the files which contain the substring instance.  However, note that, for example, if a file name is returned multiple times, it is because the instance appeared in multiple, separate lines in that specific file.  The ">" extension redirected the output into a text file called "grep-results.txt", of which the contents are shown in the last screenshot.

<br>

David Sanchez / d4sanchez@ucsd.edu
