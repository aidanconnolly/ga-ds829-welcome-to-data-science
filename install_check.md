# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Install Check (15 Minutes)

## Part 1. Operating System

While you can be a data scientist on any operating system, most practicing data scientists choose a Unix-type operating system, typically either Apple's OS X or a popular Linux distribution such as Ubuntu.

If you are already using Mac or Linux, great! Skip ahead to Part 2 and get started with your installs.

If you are using a Windows machine, we'll need to install an additional piece of software to provide a similar development environment to your OS X and Linux classmates. Go to [https://gitforwindows.org/](https://gitforwindows.org/) and download the Git Bash shell. This emulates _most_ of common commands and functions that come natively on OS and Linux systems.

## Part 2. Anaconda (Python 3) Installation

In our class, we'll be working closely with tools that utilize the Python programming language. Anaconda is a popular cross-platform tool that helps install and manage Python-related data science libraries.

1. Download [Anaconda](https://docs.anaconda.com/anaconda/install/) and follow the installation instructions package for your operating system. Make sure that you are downloading the latest stable version for Python 3!

2. Agree to the terms and let Anaconda go through its default installation. On OS X, there is a graphical installer.

3. Once installed, navigate to your command line (on OS X, this is the Terminal application, on Windows, use the Git Bash Shell) and confirm that it is installed by typing in the command `which conda`. 

  - If the command line returns a filepath (like the example below), you've successfully installed Anaconda
  - If the command line returns nothing (and sends you back to the prompt), check in with your instructor.

You should see:

```bash
$ which conda
/Users/USERNAME/anaconda3/bin/conda
```

  - **Note**: your file path may look differently
  - **Note**: you'll often see commands that look like `$ which conda` above -- on your own machine, type in everything **except** the dollar sign, which denotes the prompt in your window. 

4. Once installed, run the following command to ensure that some frequently used libraries are installed. Anaconda may also update your packages at this time (which is perfectly ok!).

```bash
conda install jupyter notebook python matplotlib nltk numpy pip setuptools scikit-learn scipy statsmodels
```

## Part 3. Git Configuration

1. To check if your git installation is successful, open a new terminal window and try to run git from the command line:

```bash
$ git --version
```

The output should be something like this:

```bash
$ git --version
git version 2.5.0
```

2. Next, you'll need to tell git your name and email. Make sure to use the same email address that you registered at [https://git.generalassemb.ly](https://git.generalassemb.ly):

```bash
$ git config --global user.name "Your Name"
$ git config --global user.email your.name@example.com
```

These identifiers will be added to your commits and show up when you push your changes to [https://git.generalassemb.ly](https://git.generalassemb.ly) from the command line!

### Optional -- Set up SSH for Easier Connection to Remote

While you can connect your local repositories (the work on your laptop) to remote repositories (those stored on [https://git.generalassemb.ly](https://git.generalassemb.ly)) without doing much additional work, this will prompt you to input your user name and password frequently. There is an alternative known as SSH that will let you create a file on your computer that will authenticate you to [https://git.generalassemb.ly](https://git.generalassemb.ly) without inputting your username and password over and over. 

**Note**: These steps are optional!

#### Using SSH and SSH Agent (recommended)

You can use these guides to get started:

- [Working with SSH key passphrases](https://help.github.com/articles/working-with-ssh-key-passphrases/)
- [Generating a new SSH key and adding it to the ssh-agent](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)
- [Adding a new SSH key to your GitHub account](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

#### What is Secure Shell (SSH)

SSH, or Secure SHell, is a common means of adding an additional layer of security. SSH is used to establish authenticity between a client and a server so that a secure connection can be formed. This can be useful for secure file sharing or remote application access.

#### How SSH works

There are a couple of steps to the SSH process at a high level:

- Client makes a request to the server.
- Server responds asking for authentication.
- Client provides authentication.
- If authentication is correct, a connection is established.
