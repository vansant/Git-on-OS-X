Git-on-OS-X
===========

Installing Git on OS X Mavericks

##Download Git 
Visit hhttp://git-scm.com/downloads to get the most recent version of the Git. At the time of this writing it is version 1.9.2 and the OS X download is named git-1.9.2-intel-universal-snow-leopard.dmg.

##Git Installation - Standard
Open git-1.9.2-intel-universal-snow-leopard.dmg and double click on git-1.9.2-intel-universal-snow-leopard.pkg and follow the on screen instructions.

##Git Installation - Without Admin Rights

###Install Git Binaries from the Apple Disk Image (.dmg) to ~/git (change this to your preferred path)

Mount the git-1.9.2-intel-universal-snow-leopard.dmg and drag the git-1.9.2-intel-universal-snow-leopard.pkg to the desktop.

Run in terminal: 
* $cd Desktop
* $pkgutil --expand git-1.9.2-intel-universal-snow-leopard.pkg folder
* $cd folder
* $cp git.pkg/Payload files.gz
* $gunzip files.gz
* $cpio -iv < files
* $mkdir ~/git
* $cp -r ./* ~/git/
* $rm -rf ~/Desktop/folder
* $rm -rf ~/Desktop/git-1.9.2-intel-universal-snow-leopard.pkg

### Add Git to $PATH
Run in terminal:
* $nano ~/.bash_profile
* Add the following export statments
* PATH = $PATH:~/git/bin
* Close and reopen terminal to use git command from terminal

