![act-logo](https://raw.githubusercontent.com/wiki/nektos/act/img/logo-150.png)
# Overview

[GitHub CLI](https://docs.github.com/en/github-cli/github-cli/about-github-cli) Extension for [nektos/act](https://github.com/nektos/act) which allows you to run your [GitHub Actions](https://developer.github.com/actions/) locally!

# How Does It Work?

When you run `act` it reads in your GitHub Actions from `.github/workflows/` and determines the set of actions that need to be run. It uses the Docker API to either pull or build the necessary images, as defined in your workflow files and finally determines the execution path based on the dependencies that were defined. Once it has the execution path, it then uses the Docker API to run containers for each action based on the images prepared earlier. The [environment variables](https://help.github.com/en/actions/configuring-and-managing-workflows/using-environment-variables#default-environment-variables) and [filesystem](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners#file-systems) are all configured to match what GitHub provides.

Let's see it in action with a [sample repo](https://github.com/cplee/github-actions-demo)!

![Demo](https://github.com/nektos/act/wiki/quickstart/act-quickstart-2.gif)

To learn more, check out the [README.md](https://github.com/nektos/act/blob/master/README.md) for nektos/act.

# Installation

To install, run: `gh extension install nektos/gh-act`
