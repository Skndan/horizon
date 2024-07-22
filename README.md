# Horizon

### Cloning the Repository
To clone this repository along with its submodules, use the following command:
```shell
git clone --recursive-submodules https://github.com/Skndan/horizon.git
```

### Add new submodule
To add a new submodule from the existing repo, use
```shell
git submodule add <new submodule git link>
```
Please ensure that the repo is already initialized

### Remove existing submodule
To remove a existing submodule from the existing repo, use
```shell
git rm --cached <submodule name>
```
Use when fatal error occurs when ``git add .``


### Pushing Changes
To push changes to the main branch, use:
```shell
git push origin main
```

### Updating Submodules
To initialize and update submodules, run:
```shell
git submodule update --init --recursive
```
To update submodules to the latest commit, use:
```shell
git submodule update --remote
```

### Checking Status
To see the status of your repository, including submodules, use:
```shell
git status
```

This command shows if there are any new commits in the submodule without a summary. To get a short summary of the commits and changes in the submodule, configure your Git settings with:
```shell
git config status.submodulesummary 1
```

### Committing and Merging Submodule Changes
After committing your changes to the submodules, switch to the main repository directory and run:
```shell
git submodule update --remote --merge
```
Validate your changes and check if your submodule changes are pushed properly with:
```shell
git push --recurse-submodules=check
```
To set the recursive check as the default, configure your Git settings with:
```shell
git config push.recurseSubmodules check
```
If you want to push all the submodule changes only, use:
```shell
git push --recurse-submodules=on-demand
```

### Configuring Diff for Submodules
To configure Git to show diffs for submodules, use:
```shell
git config --global diff.submodule log
```
Then, running git diff will include diffs from the submodules:
```shell
git diff
```
