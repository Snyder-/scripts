# Portable Scripts for Unix (OS X)

* [howtoscript](#howtoscript)
* [rubyporo](#rubyporo)


##Disclaimer 

    These are my personal scripts which have dependencies, such as Rspec, Git, Rubocop, Ruby, etc...
    DON'T expect them to work out fo the box without tweaking them or installing the dependencies.

## howtoscript

Just a script to remind you of the steps needed to create and run your own scripts.
##### Command
``` bash
%howtoscript
```
##### Output
```
How To Create An Executable Script!

If you want a script to be accessed in any folder, you must add it's directory
to the shells lookup path.

If you have scripts in the base /scripts directory, you must add it to $PATH
inside one of your .zshrc files.

Even children directories of /scripts must be added to $PATH.
If you were to make a /scripts/git-scripts/ directory, anything inside won't
be globally accessible until that folder is added to $PATH.

1. Make sure the script is either in /scripts or
2. Create a new directory and add it to $PATH.

-----------------------------------------------------
  Adding a new folder to $PATH
-----------------------------------------------------
Example Case:
    Create Folder:
      mkdir Runnables
    Add to your zshrc.local (or shell of choice ie. bashrc):
      export PATH="$HOME/Runnables:$PATH"
    Source your .zshrc.local or restart terminal

-----------------------------------------------------
  Making Scripts Executable
-----------------------------------------------------
Each script needs to be given permissions to run.  This is done
with the chmod command.

    chmod +x scripts/filename

-----------------------------------------------------
  Shebanging Your Scripts
-----------------------------------------------------
It's a good idea to place these at the top of your script to allow
for a more portable script.  This allows the shell to use a binary
loader to load the interpreter passed in. This means you can leave off
file extensions and the file will still run with specified Shebang.
loader to load the interpreter passed in.

Example Cases:
    #!/usr/bin/env ruby
    #!/usr/bin/env bash
    #!/usr/bin/env sh
```

##rubyporo

### Command
```
%rubyporo
```
In Current Folder:
  1. Checks for Rspec folders and installs if not found.
  1. Checks for Rubocop config and installs if not found.
  1. Creates repository/initial commit if git repository isn't found.
