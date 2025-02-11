# Setting Up  
***Guides to setting up git.*** 

## Introduction
These guides assume you are using a Windows operating system, but points out where there will be differences for Mac and what that might imply.

There are four steps:
1. [Get a GitHub Account](#step1)
2. [Install Git](#step2)
3. [Set Credentials (username and email)](#step3)
4. [Set Personal Access Token](#step4) 

## Step 1: Get a GitHub Account <a name="step1"></a>
To work with GitHub you will need an account. We do not provide a guide on that here, but see [this excellent written guide](https://happygitwithr.com/github-acct) which makes good suggestions on the key issues and things to think about. 

GitHub also has its own guide [here](https://docs.github.com/en/get-started/onboarding/getting-started-with-your-github-account).

## Step 2: Install Git <a name="step2"></a>
James' video on doing this on Windows: 
[![Watch the video](https://img.youtube.com/vi/SQYWigyBaAw/maxresdefault.jpg)](https://youtu.be/SQYWigyBaAw)

A step-by-step guide written by Chat-GPT (in response to the request _"write a step-by-step guide in markdown for installing git on Windows"_) is presented below (with minor edits to match the video above). 

There's also a useful guide at [Happy Git with R](https://happygitwithr.com/install-git).

### How to Install Git on Windows

Follow this step-by-step guide to install Git on a Windows system.

#### a. Download Git for Windows
- Go to the official Git website: [https://git-scm.com/](https://git-scm.com/)
- Click on **Download for Windows**. The website will automatically provide the latest version for your system.

#### b. Run the Installer
- Locate the downloaded `.exe` file (usually in your `Downloads` folder).
- Double-click the file to start the installation process.

#### c. Follow the Installation Wizard
The installation wizard will guide you through several options:

##### Select Destination Location
- Choose the installation folder or leave it as the default (installing in `Program Files` like the following is best: `C:\Program Files\Git`).
- Click **Next**.

##### Select Components
- Keep the default selection or choose additional components if needed.
- Recommended: Ensure **Git Bash** and **Git GUI** are selected (And add **Git Bash Profile** for Windows Terminal if on Windows 11).
- Click **Next**.

##### Select Start Menu Folder
- Leave the default setting and click **Next**.

##### Choosing Default editor for Git
- Pick your preferred text editor if shown. If you don't know which to pick, select Notepad
- Click **Next**.

##### Adjust name of initial branch**
- Leave the default setting and click **Next**.

##### Adjust PATH Environment
- Choose **Git from the command line and also from 3rd-party software** (recommended for full functionality).
- Click **Next**.

##### Choosing the SSH executable
- Select **Use bundled OpenSSH**.
- Click **Next**.

##### Choose HTTPS Transport Backend
- Select **Use the OpenSSL library**.
- Click **Next**.

##### Configure Line Ending Conversions
- Choose **Checkout Windows-style, commit Unix-style line endings** (recommended for cross-platform compatibility).
- Click **Next**.

##### Configure Terminal Emulator
- Select **Use MinTTY (default terminal for Git Bash)**.
- Click **Next**.

##### Choose the default behavior of `git pull`  
- Select **Fast-forward or merge**
- Click **Next**

##### Choose a credential helper  
- Select **Git Credential Helper**
- Click **Next**

##### Configure Extra Options
- Leave default selections unless you have specific preferences.
- Click **Install** to begin the installation process.

#### d. Complete the Installation
- Once the installation finishes, click **Finish**.
- You can launch Git Bash or Git CMD from the Start menu.

#### e. Verify Installation
To ensure Git is installed correctly:

1. Open **Git Bash** or **Command Prompt**.
2. Type the following command and press **Enter**:
   ```sh
   git --version
   ```
3. You should see output similar to:
   ```sh
   git version 2.47.1 
   ```

Congratulations! 🎉 Git is now installed on your Windows system.


## Step 3: Set Credentials (username and email) <a name="step3"></a>
James' video on doing this on Windows: 
[![Watch the video](https://img.youtube.com/vi/oxPh4szGILs/maxresdefault.jpg)](https://youtu.be/oxPh4szGILs)

A step-by-step guide written by Chat-GPT (in response to the request _"write a step-by-step guide in markdown for setting username and email for git from the command line"_) is presented below. There's also a useful guide at [Happy Git with R](https://happygitwithr.com/hello-git)

### Setting Username and Email for Git from the Command Line

To set your username and email for Git from the command line, follow these steps:

#### a. Open your terminal or command prompt
Depending on your operating system, you can use:
- **Windows**: Git Bash
- **macOS**: Terminal
- **Linux**: Terminal

#### b. Set your global Git username
Run the following command to set your Git username globally. This means it will apply to all your repositories unless overridden in a specific repository.

```bash
git config --global user.name "Your Name"
```

- Replace `"Your Name"` with the username you want to use in Git.

#### c. Set your global Git email
Run the following command to set your Git email globally. This email will be associated with your commits in all repositories unless overridden.

```bash
git config --global user.email "your.email@example.com"
```

- Replace `"your.email@example.com"` with the email address you want to use.

#### d. Verify your settings
To confirm that your username and email have been set correctly, use these commands:

```bash
git config --global user.name
git config --global user.email
```

This will display the username and email you've configured.

#### [OPTIONAL] e. Set username/email for a specific repository (optional)
If you want to set a different username or email for a specific repository, navigate to that repository in your terminal and use the following commands without the `--global` flag:

```bash
git config user.name "Different Name"
git config user.email "different.email@example.com"
```

#### f. Check configuration details
To see all Git configurations (both global and local), run:

```bash
git config --list
```

This will display a list of all the configuration values Git is using.


## Step 4: Set Personal Access Token <a name="step4"></a>
James' video on doing this on Windows: 
[![Watch the video](https://img.youtube.com/vi/ftHp2SXnTRM/maxresdefault.jpg)](https://youtu.be/ftHp2SXnTRM)

A step-by-step guide written by Chat-GPT (in response to the request _"write a step-by-step guide in markdown for setting up a Personal Access Token (classic) for git on Windows by cloning a private repo and using the pop-up GUI to set the Token"_) is presented below (with minor manual edits). There's also a useful guide at [Happy Git with R](https://happygitwithr.com/https-pat) and one at [gitscripts](https://gitscripts.com/git-personal-access-token).

Links in the video:
- [Password managers](https://uk.pcmag.com/password-managers/4296/the-best-password-managers)
- [OSX Keychain](https://support.apple.com/en-gb/guide/keychain-access/welcome/mac)

### Setting Up a Personal Access Token (Classic) for Git on Windows

Follow this step-by-step guide to set up a **Personal Access Token (PAT)** for authenticating with Git when cloning a private repository on Windows.

#### a. Generate a Personal Access Token (PAT)
1. Open your web browser and go to **GitHub**: [https://github.com/settings/tokens](https://github.com/settings/tokens)
2. Click **Generate new token** (classic).
3. Give your token a **descriptive name**.
4. Set an **expiration date** (recommended: 30 days for security).
5. Under **Select scopes**, choose:
   - `repo` (for full repository access)
   - `workflow`
   - `user`
6. Scroll down and click **Generate token**.
7. **Copy the token** and store it securely (you won’t be able to view it again). James' suggests using a [password manager](https://uk.pcmag.com/password-managers/4296/the-best-password-managers).

#### b. Clone the Private Repository
1. Open **Git Bash**, **Command Prompt**, or **PowerShell**.
2. Navigate to the directory where you want to clone the repository:
   ```sh
   cd path/to/your/directory
   ```
3. Run the clone command:
   ```sh
   git clone https://github.com/your-username/private-repo.git
   ```
   Replace `your-username` and `private-repo.git` with your actual GitHub username and repository name (or copy from the HTTPS option from the green button on the repo page on GitHub).

#### c. Enter Your Credentials
1. A **Connect to GitHub pop-up** will appear.
2. Click **Token**.
3. Paste your **Personal Access Token**.
4. Click **Sign In** to authenticate and start cloning.

#### d. Verify Authentication
Once cloning is complete, navigate into your repository:
```sh
cd private-repo
```
Run the following command to ensure Git is using your stored credentials:
```sh
git remote -v
```
If everything is correct, you should see the repository URL listed.

#### e. Using PAT for Future Git Operations
For future operations (push, pull, etc.), Git will use the saved token (in Windows with will be using Windows Credentials, on Mac it will be using OSX Keychain). If authentication fails, repeat the steps to generate and set a new token (you will need to do this every time your PAT expires, if you set an expiry duration).

You're all set! 🎉 Now you can securely work with your private repositories using a Personal Access Token on Windows. 🚀

---
_[James Millington](https://github.com/jamesdamillington), Feb 2025_