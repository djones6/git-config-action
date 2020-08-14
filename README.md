# git-config-action

Github Action to configure the git command line with user credentials for github.com.
This allows future steps to perform commands such as `git clone` and `git push` without needing to pass credentials at the command line.
Credentials are configured using `git config --global`, which will persist between steps within a job, but not between jobs.

A GitHub access token is used for authentication and this identifies the account, rather than a username and password.

### Required inputs:
- `user-email`: E-mail to use for git commit. This is used to associate the commit with an account in GitHub.
- `gitops-token`: A GitHub access token to use. Must include the `repo` scope in order to push commits.

### Optional inputs:
- `user-name`: Name to use for git commit. Defaults to `GitOps Update`
