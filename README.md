# gofe5

This project uses Git with gitflow.

- Fork repo from `https://github.com/vkatrenko/gofe5`

- Clone your newly created fork
```
git clone https://github.com/[username]/gofe5
```
- Your clone will automatically set a remote to `origin`
- You now need to add a new remote repo to gofe5 original

### Using Gitflow

#### Install gitflow
Now you will have everything you need to [start installing `git flow`](http://danielkummer.github.io/git-flow-cheatsheet/index.ru_RU.html).
For more information of using visit [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/) or [Work git flow clear](http://hcbogdan.com/2015/03/10/git-flow/0.

#### Init gitflow

Change directory into the project folder

```
git flow init
```
```
git remote add upstream git@github.com:vkatrenko/gofe5.git
```
```
git checkout master
```


#### Creating a feature branch

0. To start on a new feature
```
git checkout develop
```
```
git pull --rebase upstream develop
```
Start a new feature based on the develop branch
```
git flow feature start [featureName]
```

- Make your changes in the feature branch only! **develop branch should be kept clean**

- When finished (should be in feature branch). Note: we do not use `git flow feature finish`
```
git add -A :/[folder|files]
```
```
git commit -m "[message]"
```
Merge in changes from upstream develop
```
git checkout develop
```
```
git pull --rebase upstream develop
```
```
git checkout feature/[featureName]
```
```
git rebase develop
```
```
git push -f
```
Push to origin
```
git push origin feature/[featureName]
```

- Create a **Pull Request** by logging to `https://github.com/[username]/gofe5/pulls`

  - At this point, you should be notified if it will merge in without conflict
  - You also should ***code review*** your changes before submitting a pull request
  - Your lead should be notified about your request after you submit


#### Base info

[Update fork](https://toster.ru/q/218548)
