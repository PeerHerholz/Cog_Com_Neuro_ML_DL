# Setup for the course

There are a few things you need to get working on your machine in order to follow this course. However, don't worry as it's all gonna be [open source](https://en.wikipedia.org/wiki/Open_source), won't require a lot of storage and will be explained in detail.

While same parts and section will be do-able via `cloud computing`, which is nice and easy to follow in an interactive manner, it's not recommended as getting `Python` & friends to work reliably on your machine is going to be very beneficial. This holds true for the course and especially beyond. Via installing these tools, you will be equipped to basically continue right away and start using them in your everyday research workflow. This even applies if you won't continue with `python` (I certainly hope you do.) and instead work with `R` (of course also cool), `matlab` (weeeeeeeell...) or what have you.  Having that in mind and integrating other tools/resources focusing open and reproducible (neuro-/data) science, you will find a rather comprehensive set of install instructions below. While not all of them might be totally necessary for the course, they all will help you a great deal going further and are especially useful/needed if we have to hold the course virtually due to the COVID-19 pandemic.  

Don't worry, you got this!

![logo](https://media1.tenor.com/images/f72cb542d6b3e3c3421889e0a3d9628d/tenor.gif?itemid=4533805)\
<sub><sup><sub><sup>https://media1.tenor.com/images/f72cb542d6b3e3c3421889e0a3d9628d/tenor.gif?itemid=4533805</sup></sub></sup></sub>


## General things

There are a few computing requirements for the course that are absolutely necessary (beyond the few software packages you should install, described below):

1. You must have administrator access to your computer (i.e., you must be able to install things yourself without requesting IT approval).
1. You must have at least 20 GB of free disk space on your computer (but we would recommend more, to be safe).
1. If you are using Windows you must be using Windows 10; Windows 7 and 8 will not be sufficient for this course.

If you foresee any of these being a problem please reach out to one of the instructors for what steps you can take to ensure you are ready for the course start.

## Required software

To get the most out of the course, we ask that you arrive with the following software already installed:

- A command-line shell: `Bash`
- A version control system: [Git](https://git-scm.com/) & [DataLad](https://www.datalad.org/)
- A remote-capable text editor: [VSCode](https://code.visualstudio.com/)
- A literature & reference manager: [Zotero](https://www.zotero.org/)
- `Python 3` via `Miniconda`
- A [GitHub](https://github.com/) account
- [Discord](https://discord.com/)
- A `modern browser` (e.g. [Chrome](https://www.google.com/chrome/index.html), or [Firefox](https://www.mozilla.org/en-CA/firefox/new/))

If you already have all of the above software tools/packages installed, or are confident you’ll be able to install them by the time the course starts, you can jump straight to [checking your install](#checking-your-install).
The rest of this page provides more detail on installation procedures for each of the above elements, with separate instructions for each of the three major operating systems (`Windows`, `Mac OS`, and `Linux`).

### Some quick general notes on instructions

- There is no difference between `Enter` and `Return` in these instructions, so just press whatever the equivalent on your keyboard is whenever one is stated
- If you already have some of these things installed on your computer already that should (theoretically) be okay.
  However, you need to make sure that you are able to complete the steps described in [checking your install](#checking-your-install) without issue.
  - For example, having multiple different `Python` installations on your computer can lead to incredibly frustrating issues that are very difficult to debug.
    As such, if you have already installed `Python` via some other application (not `Miniconda`/`Anaconda`), it's strongly encouraged to uninstall it before following the instructions below.
    You _must_ have `Python` installed via `Miniconda` for this course.

### OS-specific installation instructions

Select the tab that corresponds to your operating system and follow the instructions therein.

```{tabbed} Windows
**Windows Subsystem for Linux (WSL)**

1. Search for `Windows Powershell` in your applications; right click and select `Run as administrator`.
   Select `Yes` on the prompt that appears asking if you want to allow the app to make changes to your device.
2. Type the following into the Powershell and then press `Enter`:

        Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

3. Press `Enter` again when prompted to reboot your computer.
4. Once your computer has rebooted, open the Microsoft Store and search for "Ubuntu."
   Install the program labelled "Ubuntu 18.04" (not "Ubuntu 16.04" or "Ubuntu") by clicking the tile, pressing `Get`, and then `Install`.
5. Search for and open Ubuntu from your applications.
   There will be a slight delay (of a few minutes) while it finishes installing.
6. You will be prompted to `Enter new UNIX username`.
   You can use any combination of alphanumeric characters here for your username, but a good choice is `<first_initial><last_name>` (e.g., `jsmith` for John Smith).
   You will then be prompted to enter a new password.
   (Choose something easy to remember as you will find yourself using it frequently.)
7. Right click on the top bar of the Ubuntu application and select "Properties".
   Under the "Options" tab, under the "Edit Options" heading, make sure the box reading "Use Ctrl+Shift+C/V as Copy/Paste" is checked.
   Under the "Terminal" tab, under the "Cursor Shape" heading, make sure the box reading "Vertical Bar" is checked.
   Press "Okay" to save these settings and then exit the application.

(The above step-by-step WSL instructions are distilled from [here](https://docs.microsoft.com/en-us/windows/wsl/install-win10) and [here](https://docs.microsoft.com/en-us/windows/wsl/initialize-distro).
If you have questions during the installation procedure those resources may have answers!)

From this point on whenever the instructions specify to "open a terminal" please assume you are supposed to open the Ubuntu application.

**Bash shell**

You already have it, now that you’ve installed the WSL!

**Git**

You already have it, now that you’ve installed the WSL!

**DataLad**

Please follow the [fantastic install instructions of the `DataLad handbook`](http://handbook.datalad.org/en/latest/intro/installation.html#installation-and-configuration). 

**VSCode**

1. Go to https://code.visualstudio.com/ and click the download button, then run the `.exe` file.
1. Leave all the defaults during the installation with the following exception:
      - Please make sure the box labelled "Register Code as an editor for supported file types" is selected

**VSCode extensions**

1. Open the Ubuntu application.
1. Type `code .` into the terminal and press `Enter`.
   You should see a message reading "Installing VS Code Server" and then a new windows will open up.
1. Press `Ctrl+Shift+P` in the new window that opens and type "Extensions: Install extensions" into the search bar that appears at the top of the screen.
   Select the appropriate entry from the dropdown menu that appears (there should be four entries; simply select the one that reads "Extensions: Install extensions").
1. A new panel should appear on the left-hand side of the screen with a search bar.
   Search for each of the following extensions and press `Install` for the first entry that appears. (The author listed for all of these extensions should be "Microsoft".)
      - Python (n.b., you will need to reload VSCode after installing this)
      - Live Share (n.b., you may need to press "Ctrl/Cmd+Shift+P" and type "install extensions" again after installing this)
      - Live Share Extension Pack
      - Docker
      - Remote - WSL

**Zotero**

1. Go to https://www.zotero.org/ and click the "Log in" button followed by the "Register for a free account" button on the subsequent page.
2. Register for a free account via providing the necessary information. N.B.: Think about the email address you are using for the registration. While it might seem feasible/appropriate to use your university account, please remember that you won't have access to it anymore after you finished your studies. Obviously, you could just change it when the time comes but you could also just use a different one right away (which might be less prone to problems anyway). 
3. Download the [Zotero Desktop App for windows](https://www.zotero.org/download/client/dl?channel=release&platform=win32&version=5.0.96.3) from the [Download page](https://www.zotero.org/download/), run the downloaded `.exe` file and follow the instructions on your screen.
4. Open the `Zotero Desktop App`, go to `Zotero` -> `Preferences` -> `Sync` and log in with your user credentials.

**Python**

1. Open a new terminal and type the following lines (separately) into the terminal, pressing `Enter` after each one:

        wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
        bash Miniconda3-latest-Linux-x86_64.sh

1. A license agreement will be displayed and the bottom of the terminal will read `--More--`.
   Press `Enter` or the space bar until you are prompted with "Do you accept the license terms? [yes|no]."
   Type `yes` and then press `Enter`
1. The installation script will inform you that it is going to install into a default directory (e.g., `/home/$USER/miniconda3`).
   Leave this default and press `Enter`.
1. When you are asked "Do you wish the installer to initialize Miniconda3 by running conda init? [yes|no]," type `yes` and press `Enter`.
   Exit the terminal once the installation has finished.
1. Re-open the Ubuntu application.
   Type `which python` into the terminal and it should return a path (e.g., `/home/$USER/miniconda3/bin/python`).
   - If you do not see a path like this then please try typing `conda init`, closing your terminal, and repeating this step.
     If your issue is still not resolved skip the following step and contact an instructor on the #help-installation channel on the BHS Slack.
1. Type the following to remove the installation script that was downloaded:

        rm ./Miniconda3-latest-Linux-x86_64.sh


**Python packages**

Open a terminal and type the following commands:

        conda config --append channels conda-forge
        conda config --set channel_priority strict
        conda install -y flake8 ipython jupyter jupyterlab matplotlib numpy pandas scipy seaborn pingouin statsmodels plotly
```

```{tabbed} Linux
**Bash shell**

You already have it!
Depending on which version of Linux you’re running you may need to type `bash` inside the terminal to access it.
To check whether this is necessary, follow these steps:

1. Open a terminal and type `echo $SHELL`.
   If it reads `/bin/bash` then you are all set!
   If not, whenever the instructions read "open a terminal," please assume you are to open a terminal, type `bash`, and the proceed with the instructions as specified.

**Git**

You may already have it; try typing `sudo apt-get install git` (Ubuntu, Debian) or `sudo yum install git` (Fedora) inside the terminal.
If you are prompted to install it follow the instructions on-screen to do so.

**DataLad**

Please follow the [fantastic install instructions of the `DataLad handbook`](http://handbook.datalad.org/en/latest/intro/installation.html#installation-and-configuration). 

**VSCode**

1. Go to https://code.visualstudio.com/ and click the download button for either the .deb (Ubuntu, Debian) or the .rpm (Fedora, CentOS) file.
1. Double-click the downloaded file to install VSCode.
   (You may be prompted to type your administrator password during the install).

**VSCode extensions**

1. Open the Visual Studio Code application.
1. Press `Ctrl+Shift+P` in the new window that opens and type "Extensions: Install extensions" into the search bar that appears at the top of the screen.
   Select the appropriate entry from the dropdown menu that appears (there should be four entries; simply select the one that reads "Extensions: Install extensions").
1. A new panel should appear on the left-hand side of the screen with a search bar.
   Search for each of the following extensions and press `Install` for the first entry that appears. (The author listed for all of these extensions should be "Microsoft".)
      - Python (n.b., you will need to reload VSCode after installing this)
      - Live Share (n.b., you may need to press "Ctrl/Cmd+Shift+P" and type "install extensions" again after installing this)
      - Live Share Extension Pack
      - Docker

**Zotero**

1. Go to https://www.zotero.org/ and click the "Log in" button followed by the "Register for a free account" button on the subsequent page.
2. Register for a free account via providing the necessary information. N.B.: Think about the email address you are using for the registration. While it might seem feasible/appropriate to use your university account, please remember that you won't have access to it anymore after you finished your studies. Obviously, you could just change it when the time comes but you could also just use a different one right away (which might be less prone to problems anyway). 
3. Download the [Zotero Desktop App for linux](https://www.zotero.org/download/client/dl?channel=release&platform=linux-x86_64&version=5.0.96.3) from the [Download page](https://www.zotero.org/download/), run the downloaded file and follow the instructions on your screen.
4. Open the `Zotero Desktop App`, go to `Zotero` -> `Preferences` -> `Sync` and log in with your user credentials.

**Python**

1. Open a new terminal and type the following lines (separately) into the terminal, pressing `Enter` after each one:

        wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
        bash Miniconda3-latest-Linux-x86_64.sh


1. A license agreement will be displayed and the bottom of the terminal will read `--More--`.
   Press `Enter` or the space bar until you are prompted with "Do you accept the license terms? [yes|no]."
   Type `yes` and then press `Enter`
1. The installation script will inform you that it is going to install into a default directory (e.g., `/home/$USER/miniconda3`).
   Leave this default and press `Enter`.
1. When you are asked "Do you wish the installer to initialize Miniconda3 by running conda init? [yes|no]," type `yes` and press `Enter`.
   Exit the terminal once the installation has finished.
1. Re-open a new terminal.
   Type `which python` into the terminal and it should return a path (e.g., `/home/$USER/miniconda3/bin/python`).
   - If you do not see a path like this then please try typing `conda init`, closing your terminal, and repeating this step.
     If your issue is still not resolved skip the following step and contact an instructor on the #help-installation channel of the BHS Slack.
1. Type the following to remove the installation script that was downloaded:

        rm ./Miniconda3-latest-Linux-x86_64.sh

**Python packages**

Open a terminal and type the following commands:

        conda config --append channels conda-forge
        conda config --set channel_priority strict
        conda install -y flake8 ipython jupyter jupyterlab matplotlib numpy pandas scipy seaborn pingouin statsmodels plotly

```

```{tabbed} MacOs
**Bash shell**

You already have it!
Depending on which version of Mac OS you’re running you may need to type `bash` inside the terminal to access it.
To check whether this is necessary, follow these steps:

1. Open a terminal and type `echo $SHELL`.
   If it reads `/bin/bash` then you are all set!

Note: If you are using Mac Catalina (10.15.X) then it is possible your default shell is NOT CORRECT.
To set the default to bash, type `chsh -s /bin/bash` in the terminal, enter your password when prompted, and then close + re-open the terminal.

**Git**

You may already have it!
Try opening a terminal and typing `git --version`.
If you do not see something like “git version X.XX.X” printed out, then follow these steps: 

1. Follow [this link](https://sourceforge.net/projects/git-osx-installer/files/git-2.23.0-intel-universal-mavericks.dmg/download?use_mirror=autoselect) to automatically download an installer.
1. Double click the downloaded file (`git-2.23.0-intel-universal-mavericks.dmg`) and then double click the `git-2.23.0-intel-universal-mavericks.pkg` icon inside the dmg that is opened.
1. Follow the on-screen instructions to install the package.

**DataLad**

Please follow the [fantastic install instructions of the `DataLad handbook`](http://handbook.datalad.org/en/latest/intro/installation.html#installation-and-configuration). 

**VSCode**

1. Go to https://code.visualstudio.com/ and click the download button.
1. Unzip the downloaded file (e.g., `VSCode-darwin-stable.zip`) and moving the resulting `Visual Studio Code` file to your Applications directory.

**VSCode extensions**

1. Open the Visual Studio Code application
1. Type `Cmd+Shift+P` and then enter "Shell command: Install 'code' command in PATH" into the search bar that appears at the top of the screen.
   Select the highlighted entry.
   A notification box should appear in the bottom-right corner indicating that the command was installed successfully.
1. Type `Cmd+Shift+P` again and then enter "Extensions: Install extensions" into the search bar.
   Select the appropriate entry from the dropdown menu that appears (there should be four entries; simply select the one that reads "Extensions: Install extensions").
1. A new panel should appear on the left-hand side of the screen with a search bar.
   Search for each of the following extensions and press `Install` for the first entry that appears. (The author listed for all of these extensions should be "Microsoft".)
      - Python (n.b., you will need to reload VSCode after installing this)
      - Live Share (n.b., you may need to press "Ctrl/Cmd+Shift+P" and type "install extensions" again after installing this)
      - Live Share Extension Pack
      - Docker

**Zotero**

1. Go to https://www.zotero.org/ and click the "Log in" button followed by the "Register for a free account" button on the subsequent page.
2. Register for a free account via providing the necessary information. N.B.: Think about the email address you are using for the registration. While it might seem feasible/appropriate to use your university account, please remember that you won't have access to it anymore after you finished your studies. Obviously, you could just change it when the time comes but you could also just use a different one right away (which might be less prone to problems anyway). 
3. Download the [Zotero Desktop App for macOS](https://www.zotero.org/download/client/dl?channel=release&platform=mac&version=5.0.96.3) from the [Download page](https://www.zotero.org/download/), run the downloaded file and follow the instructions on your screen.
4. Open the `Zotero Desktop App`, go to `Zotero` -> `Preferences` -> `Sync` and log in with your user credentials.

**Python**

1. Open a new terminal and type the following lines (separately) into the terminal, pressing `Enter` after each one:

        curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
        bash Miniconda3-latest-MacOSX-x86_64.sh


1. A license agreement will be displayed and the bottom of the terminal will read `--More--`.
   Press `Enter` or the space bar until you are prompted with "Do you accept the license terms? [yes|no]."
   Type `yes` and then press `Enter`
1. The installation script will inform you that it is going to install into a default directory (e.g., `/home/$USER/miniconda3`).
   Leave this default and press `Enter`.
1. When you are asked "Do you wish the installer to initialize Miniconda3 by running conda init? [yes|no]," type `yes` and press `Enter`.
   Exit the terminal once the installation has finished.
1. Re-open a terminal.
   Type `which python` into the terminal and it should return a path (e.g., `/home/$USER/miniconda3/bin/python`).
   - If you do not see a path like this then please try typing `conda init`, closing your terminal, and repeating this step.
     If your issue is still not resolved skip the following step and contact an instructor on the #help-installation channel of the BHS Slack.
1. Type the following to remove the installation script that was downloaded:

        rm ./Miniconda3-latest-MacOSX-x86_64.sh


**Python packages**

Open a terminal and type the following commands:

        conda config --append channels conda-forge
        conda config --set channel_priority strict
        conda install -y flake8 ipython jupyter jupyterlab matplotlib numpy pandas scipy seaborn pingouin statsmodels plotly
```

**Note**: If the instructions aren't working and you have spent more than 15-20 minutes troubleshooting on your own, reach out on the #help-installation channel on the Discord channel with the exact problems you're having.
One of the instructors will try and get back to you quickly to help resolve the situation.
If they're unable to help via `Discord`, you may be directed to attend one of the installation office hours.

### GitHub account

Go to https://github.com/join/ and follow the on-screen instructions to create an account.
It is a good idea to associate this with your university e-mail (if you have one) as this will entitle you to sign up for the [GitHub Student Developer Pack](https://education.github.com/pack) which comes with some nice free bonuses.

### Discord

Go to https://discord.com/ and download and install Discord. Please note, that you can also use Discord through your browser if you don't want to download it.
You will be invited to the course channel via e-mail.

### Modern web browser

Please install [Chrome](https://www.google.com/chrome/index.html) or [Firefox](https://www.mozilla.org/en-CA/firefox/new/).
(Safari might also work.)
Microsoft Edge is not modern, despite what Microsoft might try and otherwise tell you.


**Integrations**

A few of the tools you installed additionally nicely integrate with one another. It's of course up to you to make use of that but it's definitely recommended as it will ease up your (research/work/study) life quite a bit.

1. Go to https://www.zotero.org/download/ and install the connector for your respective browser. With that you can directly get `articles`, `books`, `blog posts`, etc. and their `meta-data` from the web and added to your `zotero` library. Please note: the `Zotero Desktop App` needs to be open for this to work. 
2. Make sure the `connector` also added the `Zotero plug in` to `google docs`, which should look like the following. Please note: the `Zotero Desktop App` needs to be open for the plug in to work.

<img align="center" src="https://www.zotero.org/support/_media/google-docs-menu.png?w=400&tok=55835d" alt="logo" title="logo" width="300" height="150" hspace=50 />
<img align="center" src="https://www.zotero.org/support/_media/google-docs-toolbar.png?w=300&tok=799a8a" alt="logo" title="logo" width="300" height="150" />

**Other cool/interesting things**

1. A [Google Chrome Extension](https://chrome.google.com/webstore/detail/citation-transparency/cepnbdbhabaljgecaddglhhcgajphbcf?hl=en) targeting citation transparency focusing gender imbalance. Going further, your `Zotero library` can also be used to [create a diversity statement](https://github.com/dalejn/cleanBib#instructions) which can be added to your written submissions. Find out more about it on [Dani Bassett](https://complexsystemsupenn.com/)'s [lab website](https://complexsystemsupenn.com/diversity-1).
2. [Grammarly](https://www.grammarly.com/): an AI powered cloud-based writing assistant that can help with typos, spelling, grammar, punctuation, clarity, engagement, and delivery mistakes. The basic version is free and integrates nicely with browsers and local apps. 
3. [GitKraken Glo Boards](https://app.gitkraken.com/glo/): create and track tasks for better project management.
4. Get a [pomodoro](https://en.wikipedia.org/wiki/Pomodoro_Technique) app that helps you to stay focus, track your work and get things done. For some examples check this [list](https://www.jotform.com/blog/best-pomodoro-app/).  

## Checking your install

Now that you've installed everything it's time to check that everything works as expected!
Type the following into your terminal:

    bash <( curl -s https://raw.githubusercontent.com/PeerHerholz/Cog_Com_Neuro_ML_DL/main/check_install.sh)

If you installed everything correctly you should see a message informing you as such.
If any problems were detected you should receive some brief instructions on what is wrong with potential suggestions on how to remedy it.
If you followed these instructions step-by-step and cannot resolve the issue please contact one of the course instructors for more help.

Yeah, you did! Great job!

![logo](https://media1.tenor.com/images/d5ebabf248130ec3842ed3b8627fd4f2/tenor.gif?itemid=4770158)\
<sub><sup><sub><sup>https://media1.tenor.com/images/d5ebabf248130ec3842ed3b8627fd4f2/tenor.gif?itemid=4770158</sup></sub></sup></sub>

## Getting the course content

Now that you have installed the required software (or not) to follow the course, it's time to gather the respective materials.

```{tabbed} Local
<img src="https://upload.wikimedia.org/wikipedia/commons/e/ea/Conda_logo.svg" alt="conda logo" width="300"/>\
<sub><sup><sub><sup>https://upload.wikimedia.org/wikipedia/commons/e/ea/Conda_logo.svg</sup></sub></sup></sub>

By installing `Python` on your system (i.e. specifically `Conda`) and setting up the appropriate environment, you will be able to open all the `Jupyter Notebooks` and go through the whole content of the course locally. 

To get things up and running, please follow these steps:

1. Download the [`environment.yml`](https://raw.githubusercontent.com/PeerHerholz/Cog_Com_Neuro_ML_DL/main/environment.yml) file (e.g. with right mouse click -> Save As). Make sure that the file ends with `.yml` and not `.txt`.
2. Open up a conda terminal (or any other terminal), and create a new conda environment with the following command: `conda env create -f /path/to/file/environment.yml` - For example ``conda env create -f ~/Downloads/environment.yml`
3. Download the notebooks in this repository via [this link](https://github.com/peerherholz/Cog_Com_Neuro_ML_DL/archive/main.zip)) and unzip them to your preferred location, e.g. `Desktop/Cog_Com_Neuro_ML_DL` or via the Download option in the respective sections.
4. Next, open up a `conda terminal` (or any other `terminal`), activate the `conda environment` with `conda activate neuro_ai` (or on older `conda environment` with `source activate neuro_ai` for `mac` and `linux` and `activate neuro_ai` for `windows`).
5. Finally, via the `terminal`, move to the folder where you've put all the unzipped content of this workshop, e.g. with the command `cd ~/Desktop/Cog_Com_Neuro_ML_DL` and run the command `jupyter notebook`. If the `notebook server` isn't automatically opened in a new browser window, please copy-paste either the `http://127.0.0.1:8888/...` or the `http://localhost:8888/...` path into a new browser window and press `Enter`. You should now see the `jupyter notebook server` (looking like a file browser and displaying the content of the directory). 
```

```{tabbed} Cloud via Mybinder

<img src="https://mybinder.org/static/logo.svg?v=fe52c40adc69454ba7536393f76ebd715e5fb75f5feafe16a27c47483eabf3311c14ed9fda905c49915d6dbf369ae68fb855a40dd05489a7b9542a9ee532e92b" alt="binder logo" width="300"/>\
<sub><sup><sub><sup>https://mybinder.org/static/logo.svg?v=fe52c40adc69454ba7536393f76ebd715e5fb75f5feafe16a27c47483eabf3311c14ed9fda905c49915d6dbf369ae68fb855a40dd05489a7b9542a9ee532e92b</sup></sub></sup></sub>


[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/PeerHerholz/Cog_Com_Neuro_ML_DL/HEAD)

[MyBinder.org](https://mybinder.org/) is a great service that allows you to run Jupyter notebooks in a `Docker` or `Python` `environment`, directly online and for free. However, this service comes of course with a restricted computational environment (1-2GB of RAM). This means, many notebooks might be very slow and some might even crash, due to not enough memory.

You can use this approach to run and test most of the notebooks and to explore the slides. To access the MyBinder instance, use [this link](https://mybinder.org/v2/gh/PeerHerholz/Cog_Com_Neuro_ML_DL/HEAD).
```

A few of the hands-on sections will require a dataset to showcase certain things. However, don't worry: we will of course only utilize `open` and `standardized` `datasets`! Moreover, we will make use of the fantastic `DataLad` to easily download the `dataset` (thus please make sure that `DataLad` is installed and works). At first, we will `install` the `dataset`:

```
mkdir data
cd data
datalad install https://github.com/OpenNeuroDatasets/ds000114.git
```

And then download (parts of) it:

```
cd ds000114
datalad get -J 4 sub-0[1237]/ses-test/anat/sub-0[1237]_ses-test_T1w.nii.gz \
                 sub-0[1237]/ses-test/func/*fingerfootlips* \
                 derivatives/freesurfer/sub-01 \
                 derivatives/fmriprep/sub-01/ses-test/func/*fingerfootlips* \
                 derivatives/fmriprep/sub-02/ses-test/func/*fingerfootlips* \
                 derivatives/fmriprep/sub-03/ses-test/func/*fingerfootlips* \
                 derivatives/fmriprep/sub-07/ses-test/func/*fingerfootlips* \
```

Finally, we will rename and move a few things:

```
mv /data/ds000114/derivatives/fmriprep/sub-01/ses-test/func/sub-01_ses-test_task-fingerfootlips_bold_space-mni152nlin2009casym_preproc.nii.gz /data/ds000114/derivatives/fmriprep/sub-01/ses-test/func/sub-01_ses-test_task-fingerfootlips_space-MNI152nlin2009casym_desc-preproc_bold.nii.gz \
             && mv /data/ds000114/derivatives/fmriprep/sub-02/ses-test/func/sub-02_ses-test_task-fingerfootlips_bold_space-mni152nlin2009casym_preproc.nii.gz /data/ds000114/derivatives/fmriprep/sub-02/ses-test/func/sub-02_ses-test_task-fingerfootlips_space-MNI152nlin2009casym_desc-preproc_bold.nii.gz \
             && mv /data/ds000114/derivatives/fmriprep/sub-03/ses-test/func/sub-03_ses-test_task-fingerfootlips_bold_space-mni152nlin2009casym_preproc.nii.gz /data/ds000114/derivatives/fmriprep/sub-03/ses-test/func/sub-03_ses-test_task-fingerfootlips_space-MNI152nlin2009casym_desc-preproc_bold.nii.gz \
             && mv /data/ds000114/derivatives/fmriprep/sub-07/ses-test/func/sub-07_ses-test_task-fingerfootlips_bold_space-mni152nlin2009casym_preproc.nii.gz /data/ds000114/derivatives/fmriprep/sub-07/ses-test/func/sub-07_ses-test_task-fingerfootlips_space-MNI152nlin2009casym_desc-preproc_bold.nii.gz \
             && cp /data/ds000114/task-fingerfootlips_events.tsv /data/ds000114/sub-01/ses-test/func/sub-01_ses-test_task-fingerfootlips_events.tsv \
             && cp /data/ds000114/task-fingerfootlips_events.tsv /data/ds000114/sub-02/ses-test/func/sub-02_ses-test_task-fingerfootlips_events.tsv \
             && cp /data/ds000114/task-fingerfootlips_events.tsv /data/ds000114/sub-03/ses-test/func/sub-03_ses-test_task-fingerfootlips_events.tsv \
             && cp /data/ds000114/task-fingerfootlips_events.tsv /data/ds000114/sub-07/ses-test/func/sub-07_ses-test_task-fingerfootlips_events.tsv \
             && rm -r /data/ds000114/*/ses-retest/* \
             && rm -r /data/ds000114/derivatives/fmriprep/*/ses-retest/* \
             && mv /data/ds000114/derivatives/fmriprep/sub-01/ses-test/func/sub-01_ses-test_task-fingerfootlips_bold_confounds.tsv /data/ds000114/derivatives/fmriprep/sub-01/ses-test/func/sub-01_ses-test_task-fingerfootlips_bold_desc-confounds_timeseries.tsv \
             && mv /data/ds000114/derivatives/fmriprep/sub-02/ses-test/func/sub-02_ses-test_task-fingerfootlips_bold_confounds.tsv /data/ds000114/derivatives/fmriprep/sub-02/ses-test/func/sub-02_ses-test_task-fingerfootlips_bold_desc-confounds_timeseries.tsv \
             && mv /data/ds000114/derivatives/fmriprep/sub-03/ses-test/func/sub-03_ses-test_task-fingerfootlips_bold_confounds.tsv /data/ds000114/derivatives/fmriprep/sub-03/ses-test/func/sub-03_ses-test_task-fingerfootlips_bold_desc-confounds_timeseries.tsv \
             && mv /data/ds000114/derivatives/fmriprep/sub-07/ses-test/func/sub-07_ses-test_task-fingerfootlips_bold_confounds.tsv /data/ds000114/derivatives/fmriprep/sub-07/ses-test/func/sub-07_ses-test_task-fingerfootlips_bold_desc-confounds_timeseries.tsv'
```


## Enter the matrix

Once you reached this point, you should be ready the enter the matrix and follow the course in your preferred way. Congrats, fantastic work!

![logo](https://media1.tenor.com/images/e5c21d98f56c4af119b4e14b6a9df893/tenor.gif?itemid=4011236)\
<sub><sup><sub><sup>https://media1.tenor.com/images/e5c21d98f56c4af119b4e14b6a9df893/tenor.gif?itemid=4011236</sup></sub></sup></sub>

