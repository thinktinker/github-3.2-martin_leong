# 3.2 GIT Authentication


### What is GitHub Authentication and how what methods available to be implemented?

GitHub Authentication verifies the identity of users by providing unique credentials to GitHub before users can access certain resources on GitHub.

GitHub Authentication methods available to be implemented as follow:
* **`Username and password only`** - Users can log in to GitHub via individual username and password, a common method for most users.

* **Two-factor authentication (2FA)** - GitHub uses an authentication code generated via a 2FA Authentication app (.e.g Google Authenticator) for someone to sign to an account on GitHub.com. Thus, the only way someone can sign into a Github account is through the 2FA authentication code on the phone after logging into the account via username and password.

* **`Passkey`** - Add a passkey to the Github account to enable a secure, passwordless login. Passkeys satisfy both password and 2FA requirements, therefore completing the sign in process with a single step.

* **`SAML single sign-on (SAML SSO)`** - gives users using GitHub Enterprise Cloud a way to control and secure access to an organization resources like repositories, issues, and pull requests. Organization owners can invite a personal account on GitHub to join their organization that uses SAML SSO, which allows the invited person to contribute to the organization whilst still retaining existing identity and contributions on GitHub.

* **`Authenticating with GitHub Desktop`** - requires installing GitHub Desktop to connect to a GitHub or GitHub Enterprise account(s).

* **`Authenticating to the API with an app`** - allow Github to authenticate a request by providing an authentication token with the required scopes or permissions. There a few different ways to get a token: 1. create a personal access token, 2. generate a token with a GitHub App, or use the built-in GITHUB_TOKEN in a GitHub Actions workflow.

* **`Authenticating to the API in a GitHub Actions workflow`** - uses an installation access token from a GitHub App to make authenticated API requests in a GitHub Actions workflow. The token can also be passed to a custom action to enable the action to make authenticated API requests.

* **`Authenticating with the command line - via HTTPS, SSH`** - this method of authenticating is determined based on whether a HTTPS or SSH remote URL is used to access and work (e.g. cloning) on a remote repository on Github.

### 15 GitHub commands and their usage

Set Your Name and Email Address. 

These settings will be used to identify user commits in the Git history.
```
git config --global user.name "[Your Name]"
```

```
git config --global user.email "[youremail@example.com]"
```
\
Stage all the files for commit to your local repository by the following command.
```
git add .
```
\
Change an existing file path and stage the move.
```
git mv [existing-path] [new-path]
```
\
Delete the file from project and stage the removal for commit.
```
git rm [file]
```
\
Commit the file that you’ve staged in your local repository.
```
git commit -m "[descriptive message]"
```
\
Unstage a file while retaining the changes in working directory.
```
git reset [file]
```
\
Push the changes in your local repository to GitHub.
```
git push origin main
```
\
Show modified files in working directory, staged for your next commit.
```
git status
```
\
Diff of what is changed but not staged.

```
git diff

```
\
Compare the file version in your working directory with the file version last committed in your remote repository. The HEAD in the git command refers to the remote repository.
```
git diff HEAD [filename]
```
\
Fetch down all the branches from that Git remote.
```
git fetch [alias]
```
\
Retrieve an entire repository from a hosted location via URL.
```
git clone [url]
```
\
Fetch and merge any commits from the tracking remote branch.
```
git pull
```
\
List your branches. a * will appear next to the currently active branch.
```
git branch
```
\
Create a new branch at the current commit.
```
git branch [branch-name]
```
\
Switch to another branch and check it out into your working directory.
```
git checkout
```
\
Merge the specified branch’s history into the current one.
```
git merge [branch]
```
\
Show all commits in the current branch’s history.
```
git log
```
### `4 GitHub commands` used most in a real project.

The 4 commands below facilitate effective collaboration, version control, and project management in a Git-based development environment.

a. Stage all changes made to files in the working directory for the next commit.

```
git add .
```

b. Records changes to the repository with a descriptive commit message.

```
git commit -m "message"
```

c. Uploads local changes to the remote repository for collaboration.

```
git push
```

d. Updates the local branch with changes from the remote repository to stay synchronized with the latest developments in the project.
```
git pull
```

## Research and References
* https://education.github.com/git-cheat-sheet-education.pdf

* https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github