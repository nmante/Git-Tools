#Utility Tools for creating a Github Repo

This repo contains some very simple shell scripts for creating, initializing and updating git repos from the command line.  I've simply combined frequently used git commands like 'add', 'commit', etc.  Fork it, and add to it if you like.


##Setup

Do these steps now to make your life easier. Trust me :)

To use these executables from any location on your computer, you need to add the directory of where you cloned this repo to your PATH variable.  You can do this by adding this to your .bash_profile file.

###Do I have a .bash_profile?

Open a new terminal and run these commands from your terminal:
	
	cd 
	ls -a

If you see .bash_profile in the list of files/dir then congrats.  Otherwise skip to the section which talks about not having a .bash_profile.

####If you have a .bash_profile

If you have a .bash_profile, then open that file with your favorite text editor and add these lines to it

	PATH=$PATH:"<the_directory_which_has_git-create_etc>"
	export PATH

Notice the quotes.  You need to have the quotes when you add it to the .bash_profile.

####If you don't have a .bash_profile

Open a new file in your favorite text editor.  Paste these commands in it:

	PATH=$PATH:"<the_directory_which_has_git-create_etc>"
	export PATH

Save it with the file name ".bash_profile".  Make sure to put the '.' at the beginning. No file extension, and no quotes.

###Explanation

Essentially, you want to be able to run these 'git-create', 'git-setup', etc. commands from anywhere.  Thus, you have to tell your computer to 'look' in the directory where you've downloaded (cloned) this repo to on your computer.

##Usage

###Create a Repo from the command line

Run this command from your terminal/commandline to create a remote repository. That means, after you run this one line, you'll have a repo show up on your github.com account.
	
	git-create <your_github_username> <repo_name>

###Explanation

	<your_github_username> - The username is what you use to login to github.com.  If you don't remember this, try going to github.com and seeing what your toolbar says.

	<repo_name> - The name that you want for the repo.  Make it anything you want.

I'm using curl to make the request and create a repo in this shell script.

###Setup the repo from the command line

Make your README, initial commit, and first push happen in one line.  Run this command to do it:

	git-setup <your_github_username> <repo_name>

###Explanation

I've simply extracted the first commands you must run for every repo, and placed them all in a shell file.  So, creating the README, adding revision, commiting it with a message and pushing to the repo are all here.

