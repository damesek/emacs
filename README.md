# 2023 Update

This page has some examples of starter scripts: https://github.com/railwaycat/homebrew-emacsmacport/blob/master/docs/emacs-start-helpers.md

The following script worked for me:

```bash
#!/bin/bash
exec $(brew --prefix)/opt/emacs-mac/Emacs.app/Contents/MacOS/Emacs.sh "$@"
```

Installing emacs-mac with brew install `emacs-mac --with-starter` will create this script automatically instead of the emacs symlink. Then starting Emacs with emacs works without the input issues.


# Compile eMacs 25.1 on Ubuntu 14.04 (installation step by step tutorials) & on Mac OSX
Please check the detailed tutorial files. 
Here come just a few basic steps. Don't forget install the dependencies too (emacs24).


1) ```sudo apt-get install build-essential```
2) sudo apt-get install build-dep emacs

If you get error message: E: Unable to locate package build-dep
Solve with this line: apt-get install lib32stdc++6 

3) sudo apt-get install emacs

4) emacs

# Adam-Arold Clojure setup summary 
// from Clojure Budapest Meetup
https://github.com/adam-arold/emacs-config-tutorial


# Other sources
Youtube video: https://www.youtube.com/watch?v=XTuzbY1YyzM </br>
Learning GNU Emacs https://www.amazon.com/Learning-Emacs-Third-Debra-Cameron/dp/0596006489

5) Mac OSX keyword fixing (!!) --- ALT (M)
from: https://github.com/frobware/cmd-key-happy

Build, Installation and Usage Instructions
==========================================

Build the application:

  $ make

Install (default is /usr/local/bin)

  $ sudo make install

Copy the sample rcfile (example-rcfile.lua) to ~/.cmd-key-happy.lua:

  $ make install-rcfile

Install the launchd configuration:

  $ make install-plist

*** BEGIN Mavericks only BEGIN ****

This last step will pop-up a dialog saying something like:
"cmd-key-happy" would like to control this computer using accesibility
features. Select "Open System Preferences" and grant "cmd-key-happy"
access.  And now you need to restart:

  $ cmd-key-happy-restart

Note: It is necessary to restart as the dialog that is popped up is
asynchronous to the running of cmd-key-happy.
