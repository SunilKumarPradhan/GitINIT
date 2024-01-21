## STEPS FOR INITIAL SETUP

1. Go to PowerShell and run this command: `winget install --id Git.Git -e --source winget`
2. `git init` - This command makes the directory a Git repository.
3. `git status` - This command is used to check the status of the repository.
4. `git --version` - This command is used to check the version of the Git installed on our system.
5. `git add .` - This command adds all the files of a repository to the staging area.
6. `git commit -m "message"` - This command is used to commit all the changes. It creates a "save point," i.e., we can revert to the old savepoint when needed.
7. `git log` - This command is used to view the history of commits of a repository.
8. `git config --global user.name "Name"` - This command is used to configure or set the user name.
9. `git config --global user.email "email id"` - This command is used to set the email.

## STEPS FOR GENERATING SSH KEYS

1. Go to the profile option on the top right corner of GitHub, and click on the "Settings" option.
2. Go to "SSH and GPG keys."
3. `ssh-keygen -t ed25519 -C "your_email@example.com"`

   **NOTE:** After executing the above command, it will ask for several things, but you have to simply press enter again and again.

   Now, we have to perform several commands on Git bash:

   - Command 1: `eval "$(ssh-agent -s)"`
   - Command 2: `ssh-add ~/.ssh/id_ed25519"`
   - Command 3: `clip < ~/.ssh/id_ed25519.pub`

4. Your SSH key is already copied to the clipboard, now go to the GitHub website and click on the "New SSH key" button.
5. Paste the copied SSH key in the Key field and give any title.
6. After confirming your password, your GitHub will look something like this.

## STEPS FOR REPO CREATION AND PULLING LOCAL DATA TO REMOTE

1. Create a Repo and give an appropriate name and description to the repository, and then click on the create repository button.
   From the interface, copy a similar command like this one:
   - Command 1: `git remote add origin [git@github.com:sunilkumar/PythonFunctions.git ]`

   **NOTE:** Stuff inside the brackets `[]` is the SSH link, replace that in your command as per your code.

2. `git branch -M main` - This command will shift you to the main branch of the repository.
3. `git push -u origin main` - This command will push all the content of your local repository to the remote repository.

[GitHub Repository](https://github.com/SunilKumarPradhan/WeaponDetection2.git)

## ERROR

To https://github.com/SunilKumarPradhan/WeaponDetection2.git
! [rejected] main -> main (fetch first)
error: failed to push some refs to 'https://github.com/SunilKumarPradhan/WeaponDetection2.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

## FIX

**STEP 1:** `git pull origin main --allow-unrelated-histories`

**STEP 2:** It might take you to the vim terminal, close the window, open bash again.

**STEP 3:**
