1. First we will create those files by using the script from the below link.
Here we will pull the file named ‘create_files.sh’ from github that consist of the script: $ wget https://raw.githubusercontent.com/k21academyuk/Bash-Scripting/main/create_files.sh
If you wish to view the file content then use the below command: $ cat create_files.sh
2. Now lets update permission and run the script to create all the files with different extensions. $ chmod +x create_files.sh $ bash create_files.sh
3. Now verify whether the files got created or not: $ ls
As we can see, the files got created.
4. Now we will organize those files inside a dedicated folder/directory based on their extensions. For that we will have to write a script that will create different directories based on the extensions and move the files accordingly inside those.
Lets pull another script file named ‘file_organizer.sh’ from github: $ wget https://raw.githubusercontent.com/k21academyuk/Bash-Scripting/main/file_organizer.sh
If you wish to view the file content then use the below command: $ cat file_organizer.sh
a. The script defines two functions:
 create_directory: This function checks if a directory exists and creates it if it doesn't.
 organize_files: This function is responsible for organizing files based on their extensions.
b. The script accepts a target directory as an argument. If no argument is provided, it uses the current directory as the target.
c. The organize_files function first checks if the target directory exists. If not, it displays an error message and exits.
d. The function then creates five subdirectories (Pictures, Music, Documents, Videos, and Misc) within the target directory if they don't already exist.
e. It loops through each file in the target directory and checks if it's a regular file (not a directory or special file).
f. For each file, it extracts the file extension using the ${file##*.} construct.
g. Based on the file extension, the script uses a case statement to determine the appropriate subdirectory and moves the file into it using the mv command.
h. The script displays messages indicating the actions taken, such as "Moving file.jpg to Pictures folder."
i. If the file has an extension not covered by the defined cases, it is moved to the Misc folder.
support@k21academy.com 30
Once all files have been processed, the script prints "File organization complete!"
5. Now lets update permission and run the script to create all the files with different extensions. $ chmod +x file_organizer.sh $ bash file_organizer.sh
Once the script runs successfully, you will see a output like above.
6. Now let’s verify if the files are organized properly or not: $ ls
As we can see different folders are created and the files are not visible outside like before.
Now lets go inside each folder to see if the files are there or not:
$ ls <Folder_Name> $ ls Documents $ ls Music $ ls Pictures $ ls Videos $ ls Misc
