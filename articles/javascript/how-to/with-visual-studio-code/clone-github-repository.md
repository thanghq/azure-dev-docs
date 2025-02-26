---
title: Clone GitHub repository with VSCode
description: Clone a public repository from GitHub to your local computer using Visual Studio Code.
ms.topic: how-to
ms.date: 01/06/2023
ms.custom: devx-track-js
---

# Clone and use a GitHub repository in Visual Studio Code

Learn the steps to clone a public repository from GitHub to your local computer using Visual Studio Code.

## Clone repository

To get started, download the sample project, `https://github.com/Azure-Samples/js-e2e-express-server`, using the following steps:

# [From command palette](#tab/create-repo-command-palette)

1. Open the command palette with the key combination of <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>. 


1. At the command palette prompt, enter `gitcl`, select the **Git: Clone** command, then select **Clone from GitHub** and press **Enter**.

    ![gitcl command in the Visual Studio Code command palette prompt](../../media/how-to-clone-github-repo/visual-studio-code-git-clone.png)

1. When prompted for the **Repository URL**, select clone from GitHub, then press **Enter**.
1. If you are asked to sign into GitHub, complete the sign-in process.
1. Enter [azure-samples/js-e2e-express-server](https://github.com/Azure-Samples/js-e2e-express-server) in the **Repository URL** field. 
1. Select (or create) the local directory into which you want to clone the project.

    :::image type="content" source="../../media/how-to-clone-github-repo/visual-studio-code-select-repo.png" alt-text="Screenshot of Visual Studio Code showing possible GitHub repos that match the text.":::

1. When you receive the notification asking if you want to open the cloned repository, select **Open**. 

# [From integrated terminal](#tab/create-repo-integrated-terminal)

1. Open an integrated terminal from **Terminal -> New Terminal**. 
1. Clone your repo with the following git command:

    ```bash
    git clone https://github.com/YOUR-NAME-OR-ORGANIZATION/YOUR-REPO-NAME
    ```

1. Change your terminal into that new subdirectory:

    ```bash
    cd YOUR-REPO-NAME
    ```

1. Then open in Visual Studio Code:

    ```bash
    code .
    ```
---

## Initialize new repository

If you don't have a GitHub repository yet, but would like to start your project locally, initialize your folder with git. 

# [From activity bar](#tab/initialize-repo-activity-bar)

1. Select source control from the activity bar, or use the key combination of <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>G</kbd>.
1. Select **Initialize repository**. 

    :::image type="content" source="../../media/how-to-clone-github-repo/visual-studio-code-initialize-repository.png" alt-text="Screenshot of Visual Studio showing the Initialize repository button.":::

# [From command palette](#tab/initialize-repo-command-palette)

1. Open the command palette with the key combination of <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>. 
1. Filter with `Git`, then select `Initialize repository`.
1. Select the folder to select as the root of the repository.

---


## Create a branch for changes 

# [From command palette](#tab/create-branch-command-palette)


1. Open the command palette with the key combination of <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>. 
1. Search for `git branch` and select `Git: Create Branch`.

    :::image type="content" source="../../media/how-to-clone-github-repo/git-cli-branch-list.png" alt-text="Search for `git branch` and select `Git: Create Branch`.":::

1. Enter a new branch name, such as `test`. 
1. The branch name is visible in the status bar. 

    :::image type="content" source="../../media/how-to-clone-github-repo/git-branch-status-bar-visual-studio-code.png" alt-text="The branch name is visible in the status bar.":::

# [From status bar](#tab/create-branch-status-bar)

1. Select the branch name in the status bar. This opens the command palette.

    The status bar is usually found at the bottom of Visual Studio code. 

1. In the command palette, select **+Create a new branch**.
1. Enter your new branch name. 

1. Enter a new branch name. The branch name is visible in the status bar. 

    :::image type="content" source="../../media/how-to-clone-github-repo/git-branch-status-bar-visual-studio-code.png" alt-text="The branch name is visible in the status bar.":::


# [From integrated terminal](#tab/create-branch-integrated-terminal)

1. Open an integrated terminal from **Terminal -> New Terminal**. 
1. Create a new branch named `MY-BRANCH` with the following git command:

    ```bash
    git checkout -b MY-BRANCH
    ```

---


## Commit changes locally

Once you have made changes on your branch, commit the changes.

# [From command palette](#tab/commit-changes-command-palette)

1. Open the command palette with the key combination of <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>. 
1. In the command palette, filter with `Git` then select `Commit`.
1. Enter your commit message, then press <kbd>Enter</kbd>.

    ![Adding the yarn.lock file to Git](../../media/how-to-clone-github-repo/visual-studio-code-commit-change.png)


# [From status bar](#tab/commit-changes-status-bar)

1. Switch to the activity bar and select the Source control icon or use the keyboard commands: <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>G</kbd>.
1. In the command palette, filter with `Git` then select `Commit`.
1. Enter your commit message, then press <kbd>Enter</kbd>.

    ![Adding the yarn.lock file to Git](../../media/how-to-clone-github-repo/visual-studio-code-commit-change.png)

---

## Push a local branch to GitHub

# [From command palette](#tab/push-command-palette)

1. Open the command palette with the key combination of <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>. 
1. In the command palette, filter with `Git` then select `Push`.
1. If you have multiple upstream remotes, select the remote then press <kbd>Enter</kbd>.


# [From status bar](#tab/push-status-bar)

1. On the Visual Studio Code status bar, select the push icon to the right of the branch name. 

    :::image type="content" source="../../media/how-to-clone-github-repo/visual-studio-code-status-bar-push-commits.png" alt-text="Visual Studio Code status bar, with the push icon highlighted.":::

1. Select the remote name from the pop-up box. If you have just one remote, you won't be asked to select the remote name. 

# [From source control extension](#tab/push-source-control-extension)

1. Select the Source Control icon from the activity bar. 
1. Select the ellipsis (...) then select: `Push` or `Push to`.

    :::image type="content" source="../../media/how-to-clone-github-repo/visual-studio-code-push-branch-to-remote.png" alt-text="Visual Studio Code source control, with the push icon highlighted.":::

1. Select the remote name from the pop-up box. If you have just one remote, you won't be asked to select the remote name. 

---

## View Git output

You can view the Git commands run when you use the Source control extension. This helps debug when a command fails. 

1. Select the Source Control icon from the activity bar. 
1. Select the ellipsis (...) then select **Show Git Output**.

    :::image type="content" source="../../media/how-to-clone-github-repo/visual-studio-code-show-git-output.png" alt-text="Visual Studio Code source control, with the Show Git Output selection highlighted.":::

## Visual Studio Code tools to work with Git and GitHub

Working in Visual Studio Code with a repository uses separate tools.

|Icon|Information|[Access from](https://code.visualstudio.com/docs/getstarted/userinterface)|
|--|--|--|
|| [Git commands](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette) in command palette|<kbd>F1</kbd>|
|:::image type="content" source="../../media/how-to-clone-github-repo/git-commit-icon-activity-bar.png" alt-text="Icon for Source control.":::|Source control extension|Activity bar|
|:::image type="content" source="../../media/how-to-clone-github-repo/github-icon-prs-issues.png" alt-text="Icon for GitHub PRs and Issues":::|[GitHub Pull Requests and Issues](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) extension|Activity bar|
||[GitHub Repositories](https://marketplace.visualstudio.com/items?itemName=GitHub.remotehub) extension|You can quickly and easily open a GitHub repository either by searching for GitHub Repositories: Open Repository... from the Command Palette, <kbd>F1</kbd>, or by choosing Open GitHub Repository... from the remote indicator (the green button in the lower left corner of the status bar).|


## Next steps

* How to [deploy a web app](../deploy-web-app.md)
* [Working with GitHub in Visual Studio Code](https://code.visualstudio.com/docs/editor/github)
* [Using Visual Studio Code with other version control providers](https://code.visualstudio.com/docs/editor/versioncontrol)
