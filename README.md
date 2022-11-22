# Bash Scripting
This example is from Codecademy's **Build a Build Script** project.

One common use of bash scripts is for releasing a “build” of your source code. Sometimes your private source code may contain developer resources or private information that you don’t want to release in the published version. 

In this example there are two folders, **source** and **build**. The objective of this script is to copy files from **source** to **build**, with a couple of exceptions and modifications.

After forking and cloning the repo, run the following commands to try:

First grant permission to run the script file
```
chmod +x release.sh
```

Now run the scipt file
```
./release.sh
```

### Quick explanation of the commands in the script file.
- Print welcome message.
- Read the first line of `changelog.md` (current release version number) into a variable `firstline`.
- Split the string `firstline` into the array `splitfirstline`.
- Save the value of the version to a variable, `version`. It is located in index 1 of the array `splitfirstline`.
- Print a statement to the terminal notifying the user of the version they are building.
- Ask the user if they need to make a change to the version.
- Assign their response to the variable `versioncontinue`.
- If the user said “1” to the continue question, proceed to copy the files. Otherwise tell them “Please come back when you are ready”.
- Iterate over all the files in the **source** directory and check if the `filename` is “source/secretinfo.md”.
- If it is, inform the user that it is not being copied. Otherwise, inform the user that it is being copied.
- After informing the user the file is being copied, copy the file into the **build** directory.
- Change the directory to the **build** directory, notify the user of the build version and list the files inside.
- Change back to the directory with the script.
