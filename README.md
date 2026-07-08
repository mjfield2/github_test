# GitHub Repository Tutorial

Michael Field

## Introduction

Git is a file tracking system that is useful for working on software with other people. Git tracks your changes locally on your computer and allows you to **save** changes to your repository on GitHub. From GitHub other users can find repositories and copy and contribute to code. We will go over some basics of Git and GitHub to get to a working level. This stuff can get very complicated and we will not cover any advanced stuff and in general, google is your best friend when dealing with Git and GitHub problems. If you know the basic operations, you can start tracking your own projects and contributing to repositories.

* Ensure you have Git and GitHub installed. If you are using a Mac, you likely have git already. You can check by opening a command prompt and typing `git`. If you have Windows you can install Git and Git Bash from https://gitforwindows.org/. Git Bash is a unix-style terminal that integrates with git.
* Ensure you have a GitHub account
* Read through this introduction https://webtuu.com/blog/04/a-laymans-introduction-to-git and set up your email address for Git so that it connects to your GitHub

**Hint: `git status` is your best friend and is a useful tool to check if you have uncommited changes, etc. I frequently use the command to stay oriented.**

## Task 1

Fork this repository, clone it to your machine, and contribute changes. Forking is the basis for collaboration and contributing to open source software. When you fork a repository, you get a copy of it in your GitHub and this version becomes yours. Forking only copies the reposity to your GitHub account. In order to get the code to your machine you will **clone** your fork. Importantly, your version of the repository will get out of date with the original and this can lead to **conflicts** when you try to **push** changes. A conflict is when you make a change to code but others have also altered the code. To avoid conflicts it is important to **pull** changes from the **upstream** repository frequently and before you make changes. After making changes to code you will make **commits**, which are bite-sized changes, and you will **push** them to your repository. Finallly to **contribute** your changes to the original repository (imagine this is an open source software with many contributors) you will make a **pull request** which essentially asks to merge your changes to the original repository.

1. In GitHub, fork this repository
2. In your fork of this repository, click the clone button to see the command and copy it or type it into your terminal and run the command *where you want the folder to be* (navigate to where you want to put the folder with `cd` in the terminal. E.g., `git clone github.com/yourusername/github_test`
3. Move into the folder in the terminal using `cd`. This folder should be tracked by Git. To check, run `git status`. Your should see a message that looks like "On branch main. Nothing to commit, working tree clean". This message tells you that Git is tracking the folder and there has been no changes.
4. Create a text file with your name, e.g., michael.txt, in the folder. Write a few sentence biography about yourself in the text file (you can use whatever text editor you want). Run the command `git status`. You should now see that there are uncommited changes.
5. Add the changes you made. Run `git add .` This is will add **all** of your uncommitted changes. You can also add individual files, e.g., `git add michael.txt`
6. Commit the change you made. We need to hit the save button before we send the changes. When you make a commit you include a short message describing what the change is. These messages are often very short. For example, I would run the command `git commit -m "created biography"`. This command is making the commit and the `-m` argument is indicating that we are adding the message that follows.
7. Run `git status`. You should now see that the change is committed.
8. Run `git push origin main`. This command will push the committed change to your repository (the one you forked). The origin means we are going to the GitHub repository that is the origin of your local folder and main is the branch that you are pushing to (you only have a main branch).
9. Run `git status`. You should now see that there are no changes waiting to be committed or pushed.
10. Go to your repository on GitHub. Check to see your change in your repository. You should see that your repository is one commit ahead of my repository. You now want to contribute your work to the original repository by making a pull request. You can do this simply by clicking the button in the blue area and making the pull request. If there are no conflicts I will then merge your changes into my repository. That is how contributions work in open source software. You now have the skills to make simple contributions to your favorite software!

## Task 2

Increase your GitHub presence by putting code that you already have on GitHub. You can follow the directions here https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github under **Initializing a Git Repository**. However before you initialize your repository follow these directions.

1. create a `README.md` (like this document). This will be the front page of your repository and you should provide plenty of information about the purpose and functionality of the repository. This is a markdown document and you can lookup the basics of formatting the text. For examples of README you can look at: https://github.com/GatorGlaciology/GStatSim/tree/main and https://github.com/mjfield2/stochastic_bathymetry
2. create a `.gitignore` file (note the period at the beggining because this is a hidden file). This file tells Git what to ignore. This is useful because we don't want to track temporary and hidden files that are always changing, or we may want to ignore raw data or output files that are too large (GitHub is not meant for storing large files. The limit is about 50 Mb). In this file, on each line put a folder or file that you want to ignore. You can use wildcards to easily filter out files you don't want. See this as an exampleL https://github.com/mjfield2/stochastic_bathymetry/blob/main/.gitignore (Note the use of the * wildcard to find any matches).
3. Run `git init -b main`
4. First add and commit and push your README and .gitignore to get started to ensure that the files are ignored later. Run `git add README.md .gitignore`. Commit those changes and push them. Check on GitHub that the changes have been pushed.
5. Add the rest of the files. Run `git add .` (The period means add everything). Commit and push the changes.
6. Add a license on GitHub. There are templates you can use on GitHub.

## Other Notes

* These are just the basics, but most of that Git and GitHub are all about.
* Branches are a powerful tool for working on different aspects of a project without screwing up the main branch.
* In general, you should try to keep commits small and make them frequently. For every task or little problem that you try to solve in your code, make a commit. This will help you avoid creating conflicts.
* Before you begin coding something fix that you want to make, run `git pull origin main` to ensure that you have all the upstream changes. If you go ahead and create conflicts you may need to abandon your changes and thus lose time.
