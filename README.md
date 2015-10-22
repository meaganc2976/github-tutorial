# GitHub Tutorial

_by Meagan Carioti_

---
## Git vs. GitHub
* Difference between **Git** and **Github**:
  * Git is _version control_. Git is a tool that keeps track of changes.
  * Github uses git or needs it to work, and is a _website or cloud_ that stores all of the code. It is also used for collaboration with others.
        
* How you use it: 
 * In order to use Github, you would go to the website github.com and set up an account. There you can visually see your work or your changes. 
 * In order to use git, you would type `git init` in the command line to set up or start up git in a certain folder. Then you would type in different git commands in order to create different projects and make changes, such as `git add`,  `git clone`,  `git commit`, and more.

---
## Initial Setup
**1.** Go to [Github](http://www.github.com) and sign up for a free account. 

**2.**  Now you have to connect your github to your local 
repository, for example, your
repository on nitrous or cloud9. 
You need to connect your **local** and your remote **repository** so you will be able to push your changes up
to github to visually see and share your work.

* In order to connect the two, you need to :
  * Go to [cloud 9](c9.io)
  * Got to settings and click on the tab labeled SSH key
  * copy the SSH key
  * Go to [Github](http://www.github.com)
  * Click on the profile icon on the top right and click on settings
  * Click on the tab labeled SSH key and add an SSH key (The title will be cloud 9)
  * Paste the SSH key in the box underneath the title
  * Now go into your cloud 9 and type in the command line: `ssh -T git@github.com`
  
(We need to type this in the command line because it confirms the connection made between the local and remote, or the connection between cloud9 and github.)

  
  If you did it correctly, you should see something like this:


    `Hi [YOUR USERNAME]! You've successfully authenticated, but GitHub does not provide shell access.`

 
**3.**  `Git config --global user.name "First Last"`
or
`git config --global user.email "Your Email"` is a 
command that sets up your username or email
and applies it to everything, or in other words, your local repo now knows your default information and will remember your username and email. You are essentially setting up your information globally and telling git what your username or email is.




---
## Repository Setup
* In order to set up your repository, you would first, `cd` into the folder or directory that you want to work on, and then typ in `git init`.

 After typing this in, you should see something like this:

  `Initialized empty Git repository in /home/ubuntu/workspace/test-repo/.git/`

* `git init` is a command that starts up or sets up git. It allows you to use git. Once this is typed in, the directory will now turn into
 something called a repository, which has verison control and will now keep track of all the changes you make.

* You can now create a file to work on.
First, you have to add it. To add, you just type in `git add [filename]`. This puts that file on a stage, or imaginary place, to be commited. We have to add a file in order to commit it. You type in the command line `git commit -m "message"` to commit that file or save that change/ save the file just the way it is at that very moment. By commiting the file, we are keeping track of the changes we make, which is helpful when editing, collaborating, and looking for bugs or errors.
Also, your message when commiting should be present tense and specific because when looking back on all the changes you did, you will only see the message you create.

* Now you have to create a new repository on Github by going to the top right, clicking on the plus sign, 
and then select new repository. The name of your repo on github **MUST MATCH THE NAME OF YOUR REPO ON YOUR CLOUD 9** (P.S. Repo is like a directory. First you make the folder or directory in your cloud9, then, after git init, the directory becomes a repository and changes will then be tracked)
  * Next, click on SSH 
  * You will see two lines of code. Copy and paste each of them, one at a time. 
    * The line of code should start off like this: `git remote add origin git@github.com/`
  and the second line of code should look like this: `git push -u origin master`
 . This is sets github as your default or place you want to send your changes to. Now, you only have to type `git push` in the command line and it will automatically know to push or send your commit to your github repository
* Your remote repository is the repository you created on github and your local repository is the one you created on cloud 9. 
You set up a connection between your local and remote. 



---
## Workflow & Commands

* `git status` is an extremely important command that should be used very often. It tells you what you have added to the stage or what needs to be commited. Frequently typing this command will help make sure that you are doing everything correctly and helps you make sure that you commit everything you need to.
* `git add` is the command that puts the file on the stage to be ready to commmit. We have to add a file in order to be able to commit it. You should use this command every few changes you make to a file, that way you can commit and save each change 
* `git commit` is the command that takes a snapshot of the code or saves that specific change you made
* `git push` pushes your commit or your change you just made to github, so that when you go to Github.com, you can visually see your work or all the changes you made. It essentially sends changes from your local to your remote repo.

---
## Collaboration

* Go to another person's repo that you want to work on _(on github)_
* Click the button fork near the top of the page
* Copy and paste url (_located on the right side of the page_). Make sure SSH is selected
  * You just forked someone's repo. This means that you sent or made a copy of a project from someone else's remote repository to your own remote repository (**Fork= remote to remote**)
* Go to your command line and type `git clone [past url here]` 
  * You just cloned someone else's project, which means you made a copy of a project from your remote repo to your local repo, so you can work on it (**Clone= remote to local**)
* Now you can make whatever changes your heart desires
* On Github, when you click on your last commit, you can click a button called pull request. This sends the original owner of that project teh change you made. The change does not go to their project automatically. They can see what change you requested and can either accept or deny. 
* `Git pull` pulls down any changes another person made. It pulls it down from your remote repository to local.