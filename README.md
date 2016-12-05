# Git-ing Started with Git

This README will give you a brief but solid introduction to `git` and Github. First, a brief introduction...

### GitHub

GitHub is an online service for hosting Git repositories. A repository is just a 'package' code. Repository's are like folders/directories on your computer, and you can put all of your code for specific projects into their respective directories. For example, we have repositories for past years' robots, as well as a repository for the robot we will be writing this year. This let's us keep all of our past code to be able to look at, while also letting us work on the new code. GitHub provides a very nice management interface, great tools for browsing your Git repositories, and good ways to find source code libraries to use. If you don’t have a GitHub account, [head over and sign up for one][1]. Other than just holding our code for us, we will also use a nice tool called `git` to let us all work on our code together while still all being on the same page with the same code, even when something is updated.

### Git

Git is probably the most popular and widespread tool out there used for collaborative software development. It allows multiple software developers to easily and effectively work together. It is a distributed revision control system with an emphasis on speed, data integrity, and support for distributed, non-linear workflows. 

Git may seem confusing at first, but it has many benefits over simpler solutions such as Dropbox. First, Git gives you control over when collaborators see your changes. This is important when developing software since you may have versions that you are not finished with and don’t want others to use yet. Dropbox forces you to share changes immediately. Second, Git allows you to attach metadata to each version of your software—describing what it does, what works and what doesn’t, etc. Dropbox lacks this feature. Finally, in many cases Git is smart enough to merge changes from multiple software developers to the same source code automatically—even if the changes modify the same files. Dropbox can’t do this either. While Google Drive and Dropbox are great for various types of collaboration, when collaborating on software you should use Git, which is why we will use it.

From here, make sure that...

1. You have a GitHub account.
2. You have `git` installed (Command line version, sorry...)
   * **MacOS**: Open up a new terminal (command line), and type `git`. Either you will have it or it will try to install it.
   * **Linux**: Open up a new terminal (command line), and type 
      ```bash
      sudo apt-get install git-all
      ```
   * **Windows**: Go to [this website][2] and download the `Git for Windows`.
3. You have access to the SJCI Robotics private repositories (You should be able to remove `git-started-with-git` from this URL and see more repositories such as 2016_Stronghold and a few others). Talk to *dstarner* on Slack for more info.

## Git Tutorial

To get, run ```git clone git@github.org:<USER ACCOUNT>/<REPOSITORY NAME>.git```

If you want a super indepth Git tutorial, read the official [here][3]

So a couple things you should know...

1. Pulling Code
2. Pushing Your Changes
3. Branches and Pull Requests

So, let's begin.

##### NOTE: ```<*VARIABLE*>``` means that There is a variable that you need to change out with something actual :D 

### Pulling Code
1. ```git clone <*REPO URL*>``` - This takes a repository (project) and copies it to your computer.
2. If you already have a project, then you can run ```git pull <*HEAD*> <*BRANCH*>```. Note that here, our HEAD will be ```origin```; the branch may change but will mostly be ```master```. This command takes the most updated code in the repository, downloads it, and puts it into your project. Note: Unless there are conflicts, it does not change any code you changed, it just appends/removes other changed code.


### Pushing Your Changes
There is a pretty solid workflow to pushing (uploading) your code to the repository. If you want more questions, then Google it.

1. ```git status``` --> This command lists all the changes since the last commit. Red means its not added to be 'pushed' (uploaded), and green means it is added.
2. ```git add <*FILENAME*>``` --> This command 'adds' a file named FILENAME to be added to be uploaded (note that it doesnt actually upload it, just says 'Hey, this is done, in the future I want it to be in the repository!')
3. ```git commit -m "Updated the Flux Capacitor"``` --> This command creates a commit (Think of it as the code being packaged together) with a description of what was done - as noted in the double quotes. These commits are what are uploaded to the repository.
4. ```git push -u <*HEAD*> <*BRANCH*>``` --> This pushes (uploads) the commits to the repository. The HEAD will almost always be origin, but the BRANCH will change based on what branch you are working on.


### Branches and Pull Requests
Branches and Pull Requests are how teams stay organized and can guarentee that their code works while still being able to test, develop, and peer review any code and changes. A branch is exactly what it sounds like, a branching-off of the repository. The default/main branch is called ```master```, and this is NEVER commited/pushed into. The master branch is also usually the Production branch in most professional enviroments, and its all the code that works perfectly. *FOR US* We will also have a ```staging``` branch, this will be where we pull request and merge all of our code into. Its the code that we are 90% sure works, but if any small changes need done, then its not too hard. After these two, there can be as many branches as you want, because for each Task/Build, you will create a new branch, so that we are all working on different branches for different tasks to avoid any issues. So besides the two main branches, other sub branches are like ```login page```, ```scoring_system```, ```controllers```...etc. Pretty much if you have a task that requires changing more than one file, CREATE A BRANCH! So how is this done?
1. ```git checkout -b <*BRANCH*>``` --> This command creates and switches to a new branch called BRANCH. At this point, you can push/pull code to this branch like any other.
2. ```git checkout <*BRANCH*>``` --> This switches to an already created branch.

So once you have a branch that you are happy with, go to BitBucket, and create a ```Pull Request``` on your branch, with a solid description/name of what you did. A Pull Request is saying that you want to merge one branch into another. In most scenarios, we will be merging your development branch into the staging branch. Then, myself or someone else in the group will look over your code to make sure it looks good, and then they will accept the Pull Request.

This is a solid start, if you have any questions then either Google it or just ask, cus its better to ask then to break something lol 

If you got this far, try it! Pull this change to your computer, and add your name to the bottom of this file (README.md) and then push it! :D
--Dan
--Minfan Wang
--Jon

[1]: https://github.com/join
[2]: https://git-for-windows.github.io/
[3]: https://www.atlassian.com/git/tutorials/setting-up-a-repository/
