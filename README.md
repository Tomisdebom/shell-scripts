1.	MYCP
I use the cat command to copy a file (in the current directory) to an output file
(in a desired directory). However a "/" is needed

2.	MYGREPCP
I use the find command to find all files in directory $1 containing the string $2
in their name. The corresponding files will be copied to a given directory $3

3.	MYDF
You can set values to PROMT_COMMAND. By using the echo -n extension, we can set the
value of df to the actual prompt. The -H extension of df outputs the value in 
Gibibyte. The grep and awk pipes filter the output of df to only output the actual 
value.

4.	KILLME
There is a feature of the killall command (-u) which kills all processes of a specific user $1.

5.	READNEWS
First I move to the root directory by using cd. After this I download the index.html
page by using the wget command. I then filter out the headlines by using grep 'a href'.
This cuts the headlines out at the right point. After this, I use the sed command to 
filter out certain types of characters. This is followed by a reversion of all characters 
using the rev command. I now cut off the last 5 characters and reverse again. The 
filtering is finalized by using grep -Ev to filter out the last line of the document. 
After all of this, I remove the current index.html file from the root directory, so that 
a new, updated, version will be ensured when running the command again.
