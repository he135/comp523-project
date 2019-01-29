# COMP 523 Team T Sample App

This is a sample project using React for learning purposes.

## Getting started
You will need to have Node.js installed beforehand.

First, clone the repo and checkout the sample branch:

```
git clone https://github.com/kylefeng28/comp523-project
cd comp523-project
git checkout sample
```

Then, use npm to download the dependencies:
```
npm install
```

Now you run the app in development mode:
```
npm start
```

Open http://localhost:3000 to view it in the browser.  
The page will reload if you make edits.  
You will also see any lint errors in the console.

## Git Branching
I would recommend having your shell show the current git branch. I recommend [fish](https://fishshell.com/), but if you use bash, you can just put the following code in your `.bashrc` as well.

<details>
<summary>Click to show code</summary>
<p>
```bash
# Courtesy of https://stackoverflow.com/a/6086978
function color_prompt {
    local __user_and_host="\[\033[01;32m\]\u@\h"
    local __cur_location="\[\033[01;34m\]\w"
    local __git_branch_color="\[\033[31m\]"
    #local __git_branch="\`ruby -e \"print (%x{git branch 2> /dev/null}.grep(/^\*/).first || '').gsub(/^\* (.+)$/, '(\1) ')\"\`"
    local __git_branch='`git branch 2> /dev/null | grep -e ^* | sed -E  s/^\\\\\*\ \(.+\)$/\(\\\\\1\)\ /`'
    local __prompt_tail="\[\033[35m\]$"
    local __last_color="\[\033[00m\]"
    export PS1="$__user_and_host $__cur_location $__git_branch_color$__git_branch\n$__prompt_tail$__last_color "
}
color_prompt
```
</p>
</details>

### Show branches
```
git branch # show local branches
git branch -r # show remote branches
```

### Switching branches
```
git checkout branch_name
```

### Creating a new local branch
From the branch you want to branch from, run:
```
git checkout -b new_branch_name
```
### Pushing a new local branch to origin
```
git push -u origin new_branch_name
```
