# Programming Workshop

## Getting Started

### Installations

You'll want to install some sort of package manager. A package manager can be used to ensure compatibility between different versions of Python and Python packages that you've installed in a particular environment.

I personally prefer Anaconda, but have used both of the following at some time or another:

- [Anaconda](https://docs.anaconda.com/anaconda/install/)
- [Homebrew](https://brew.sh/)

To keep everyone on the same page, I'll be using Anaconda for this workshop since it supports a wider range of operating systems.

I'd also recommend installing an IDE if you don't already have one that you enjoy. I use [Visual Studio Code]() since it has a variety of extensions you can install to make coding easier. If you install VS Code, I'd recommend navigating to the Extensions tab (looks like a 2x2 grid on the left menu bar) and installing Git Lens. This extension provides a nice visual depiction of file changes and various commits used in a git repository.

At this point, you should verify that Anaconda was installed properly by running the command `conda` in a command line prompt. If successful, you'll see output with a list of options for conda commands. If not, you'll see an error about how conda is an unrecognized command.
### Set Up

Once you've installed Anaconda for your operating system, you'll either want to open up a command line prompt or the Anaconda Navigator that was installed in the previous step. I prefer using the command line since it integrates nicely with VS Code and can be used for managing installations, version control via git, and running code.

If you're using the command line:

1. Create a project directory where you'll be creating files and running code from. Use the command `cd directoryLocation` to navigate to where you'd like to create the directory and then `mkdir DirectoryName` to create a new folder within the directory location. For example:
```
cd /Users/sarahmantell/Documents
mkdir MyFolder
```
will create a folder called `MyFolder` in `/Users/sarahmantell/Documents`.

2. Use the command `cd DirectoryName` to navigate to the folder you made in the previous step. Note that you do not need to use the whole path since you're already in `directoryLocation`.

3. Create a new Anaconda environment. When you create a new Anaconda environment, you can specify a version of Python to initialize the environment with. Running the command
```
conda create -n wkshp python=3.9
```
creates a new virtual environment named `wkshp` with a copy of Python version 3.9 installed. After running this command, conda will provide a list of the packages that will be installed along with the specified version of Python. When prompted with `Proceed ([y]/n)?`, type `y` and enter to install the necessary files. Conda displays progress bars at this point to show you the progress in creating the virtual environment.

4. Once you've created your new environment, run the command `conda env list` to see a list of all your environments and your locations. Mine looks like this:
```
# conda environments:
#
base                  *  /Users/sarahmantell/opt/anaconda3
mib                      /Users/sarahmantell/opt/anaconda3/envs/mib
sandbox                  /Users/sarahmantell/opt/anaconda3/envs/sandbox
```
The astricks indicates which environment is currently active. Let's activate your new environment by running the command `conda activate wkshp`. Run `conda env list` again to verify that your new environment is active.

5. Now that you've created an environment, it's time to install packages! Below is a list of packages that we'll be using and the conda command to install them.