# Source Blogdown files for the corelab.io website
This repository contains the source files for the CORE Lab webpage (corelab.io), which is just a GitHub Pages page (co-relab.github.io) with a custom domain.

The site is built in the [Blogdown R Package](https://bookdown.org/yihui/blogdown/) and this repository stores the source Blogdown files. Netlify.com then "knits" the files into .html and other web-compatible files that are published.

The workflow to edit the webpage is to fork the files to your GitHub account, clone the files locally, make any edits, commit the changes back to your GitHub account, then submit a "Pull Request" to the main co-relab/co-relab_source branch on GitHub.

Basic steps for CORE lab members to edit the webpage:  

1. Ensure you have R and R Studio installed.  
2. Create a GitHub account.   
3. [Fork](https://help.github.com/articles/fork-a-repo/) the repository into your own account:  
https://github.com/co-relab/co-relab_source  
4. If necessary, [Install Git](https://help.github.com/articles/set-up-git/) (comes with MacOS by default)  
5. [Clone](https://help.github.com/articles/cloning-a-repository/) (e.g., download the files and create a Git repository on your local hard disk) the repo locally. To do this, first go to the forked repository on GitHub, click the "Clone or Download" button, copy the link. 
Open a [Terminal](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line) (or [cmd prompt](https://www.howtogeek.com/235101/10-ways-to-open-the-command-prompt-in-windows-10/)), navigate to where you want the files to be stored on your hard disk (use the 'cd' command in Terminal, which changes your directory), and run:
`git clone <copied url>`

Replace `<copied url>` with your clipboard.

This will create a new directory on your computer: co-relab_source

6. Navigate on your computer to the new *co-relab_source* folder and open *co-relab_source.rproj* in R Studio. 
7. Also open *co-relab_source_rscript.R* (the R script). Using R Projects eliminates the need to set a working directory each time (it's automatically set to the folder containing the .rproj file).
8. In the Terminal of R Studio (or your regular command line), [configure the remote repository](https://help.github.com/articles/configuring-a-remote-for-a-fork/) so you can update your local files with changes from the main repo:  
`git remote add upstream https://github.com/co-relab/co-relab_source.git`
9. Each time before you start editing the page, [update your local repo](https://help.github.com/articles/syncing-a-fork/) and resolve any conflicts:  
`git fetch upstream`  
`git checkout master`  
`git merge upstream/master`

If you get conflicts you will have to resolve them before it will let you merge. IF you want to overwrite your local changes with the main repo
you can "stash" your files like this:
`git stash save --keep-index`

If you don't want to keep your stashed files, drop them:
`git stash drop`

10. At this point, just follow instructions in the R script to edit the page. Once you're done, you'll "Commit" those changes, "Push" them back to your fork (these steps in R Studio). Then, you'll submit a Pull Request on GitHub.com. Your changes will be live when the admin for the co-relab GitHub account merges the changes.