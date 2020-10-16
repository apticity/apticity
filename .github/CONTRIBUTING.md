# contributing

All notable contributions to this project will follow the process documented in this file.

The format is based on [Node.js Pull Request Process][nodejs],
and this project adheres to the [Contributor Covenant Code of Conduct][code_of_conduct].

## environment setup

You need to prepare your machine with the following tools.

- install `git`, _v2.28.0 or later recommended_
- install `nodejs`, _v12.19.0 or later recommended_
- install `ruby`, _v2.6.0 or later recommended_
- install `ssh`, _v8.1.0 or later recommended_
- install `vscode`, _v1.48.0 or later recommended_

Remember to configure `git` as follow:

```zsh
git config user.name '<name>'
git config user.email '<email>'
```

You are now ready to contribute. Let's start by creating a fork.

### fork

1. fork the project on [GitHub][repository]
1. clone locally your forked repository

```zsh
git clone git@github.com:<organization or username>/<repository>.git
cd <repository>
git remote add upstream git@github.com:apticity/apticity.git
git fetch upstream
```

### branch

1. create a local branch off of the `main` branch of `upstream` repository

```zsh
git checkout -b <branch> --track upstream/main
```

## contribution workflow

### code

The pull requests will largely affect the codebase as follow:

1. the `CSS, HTML, Markdown` code contained in the `jekyll` directory

### commit

1. create a commit for each logical unit of change, keeping the scope as small as possible
1. write a message which describes the change, starting with an imperative verb such as:
   - > add id property to object model
   - > fix linting errors in app module

```zsh
git add <changed files>
git commit --message '<single line message no longer than 72 characters>'
```

### rebase

1. synchronize with the `upstream` repository, keeping the local branch up-to-date

```zsh
git fetch upstream
git rebase upstream/main
```

### push

1. run `build`, `test` commands against the codebase
1. push the codebase to the remote forked repository

```zsh
git push origin <branch>
```

### pull request

1. open a pull request on the `upstream` repository
2. fill out any required information from the template

### discuss, update

1. review the feedback or request for changes on your pull request
1. make any necessary changes to your local branch and push to your remote forked repository
1. keep the local branch up-to-date with `upstream` repository

```zsh
git add <changed files>
git commit --message '<single line message no longer than 72 characters>'
git push origin <branch>
```

```zsh
git fetch upstream
git rebase upstream/main
git push origin <branch>
or
git push --force-with-lease origin <branch> (only when absolutely necessary)
```

### merge

1. the pull request needs to pass the review and approval process
1. the pull request needs to pass the continuous integration process

Thank you for contibuting to this project.

[code_of_conduct]: https://github.com/apticity/apticity/blob/main/.github/CODE_OF_CONDUCT.md "code of conduct"
[nodejs]: https://github.com/nodejs/node/blob/main/doc/guides/contributing/pull-requests.md "nodejs pull request process"
[repository]: https://github.com/apticity/apticity "apticity"
