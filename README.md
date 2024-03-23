# useful-scripts
List of useful scripts that I have used


## Create file with set size, set name, and unreadable content
While creating a truly "corrupted" file with specific content is difficult, you can create a 10MB file filled with random data, which would be effectively useless and unreadable by typical programs. Here's how:

Using dd:

    Open a terminal.

    Run the following command:

      
dd if=/dev/urandom of=corrupted_file bs=1M count=10

    

Use code with caution.

Explanation:

    dd: This command is used for data duplication and conversion.

    if=/dev/urandom: This specifies the input file. /dev/urandom is a special file that generates random data.

    of=corrupted_file: This specifies the output file name. You can change "corrupted_file" to your desired filename.

    bs=1M: This sets the block size to 1 Megabyte.

    count=10: This specifies the number of blocks to copy. 10 blocks of 1MB each will result in a 10MB file.

This command will create a 10MB file filled with random data, which will be effectively "corrupted" as it won't contain any meaningful information.

Alternatives:

    You can use other tools like head and /dev/zero to create a file filled with null characters, which would also be considered "corrupted" in most contexts.

    You can also manually write random characters to a file using a text editor, but this would be more time-consuming for larger files.

Remember that these methods create files that are not technically corrupted in the sense of data corruption during storage or transfer. They are simply filled with meaningless data, making them unusable for most purposes.
