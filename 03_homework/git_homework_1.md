# Git Homework 1

## Tasks
### Task 1
1. Create a new directory named `githomework1`.
2. Initialize an empty git repository with `git init`.
3. Using your choice of text editor, create a README.md file.
4. Using the git command line, add this file to staging, then commit the file to your repository with a suitable commit message.
    * `git add <filename>` then `git commit`
5. Write a suitable commit message and finalize your commit
6. 📸 Take a screenshot of your terminal output
   ![image](https://github.com/sabarevasan/git/assets/137091627/b60aa54f-31e5-4a01-8c9b-b55bf5da2dae)

8. Show the commit history
    * `git log`
9. 📸 Take a screenshot of your terminal output
    ![image](https://github.com/sabarevasan/git/assets/137091627/20dda4f9-7b77-4b05-8347-7efb28e9a153)


### Task 2
1. Create a new public repository on GitHub
2. Add your GitHub repository as a remote for your local `githomework1` repository
    * `git remote add origin <url>`
3. Push your local `githomework1` repository to GitHub
   `git push --set-upstream origin master`
   ![image](https://github.com/sabarevasan/git/assets/137091627/4759cad2-dfcc-4e27-8b72-590f714f81b8)

5. Include your repository URL in your submission
   `https://github.com/sabarevasan/githomework1`

### Task 3
1. Create a new branch called `playing-with-bash`
2. Create 5 empty files with the names up to you
3. Use `echo` into the 5 empty files a few sentences about anything
4. Stage, commit and push your work on GitHub
   ```bash
   #!/bin/bash
   FILENAME="filename-"
   max=5
   COMMIT_MESSAGE="commit run by bash script"
   touch play-log.txt
   
   # Setting up
   cd githomework1
   git checkout master
   git pull
   
   # create a new branch for githomework1 directory
   git checkout -b playing-with-bash
   wait
   echo "✅ CREATED new branch playing-with-bash" >> play-log.txt
   
   # create 5 empty files
   for count in `seq 1 $max`
   do
       touch ${FILENAME}${count}".txt"
   done
   wait
   echo "✅ CREATED empty files" >> play-log.txt
   
   # add text to the 5 empty files
   for count in `seq 1 $max`
   do
       echo "Random text to append to these files." > ${FILENAME}${count}".txt"
       git add ${FILENAME}${count}".txt"
   done
   wait
   echo "✅ Files now not empty" >> play-log.txt
   
   # commit and push
   git commit -m ${COMMIT_MESSAGE}
   wait 
   git push origin playing-with-bash
   wait
   echo "✅ Commit and Push complete" >> play-log.txt
   
   cd ..
   ```
6. Open up a pull request
   ![image](https://github.com/sabarevasan/git/assets/137091627/e1eacb0f-25dd-44f5-b8c7-763d455b9e88)


### Submission

1. When you are done, please commit your changes, and push it to GitHub.
2. Open up a pull request and add your Learning Support Person as a reviewer. You may need to add them to your repository.
