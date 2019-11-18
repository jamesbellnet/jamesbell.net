# jamesbell.net

My personal website.

#### Merge Changes from the Template Repository:

Add the template as a remote repository:

```
git remote add template https://github.com/jamesbellnet/webpack-basic-website.git
```

Create a new branch from master:

```
git checkout -b template-updates
```

Pull changes from the template:

```
git pull template master --allow-unrelated-histories
```

Resolve merge conflicts, stage & commit the changes then return to `master`:

```
git checkout master
```

**IMPORTANT** - merge **and squash** the changes into the master branch. **A normal merge will result in merging the commit history of both the template repository and this one.**

```
git merge --squash template-updates
```

Commit the changes:

```
git commit -m "Merged template updates"
```

Force delete the new template branch to prevent git throwing an error:

```
git branch -D template-updates
```
