# git-aliases  
Adding Git Aliases  
Aliases live in the section `[alias]`  

Editing the global config file, which is located at `~/.gitconfig` or aliases can be set scoped to a project.  

Open the `.gitconfig`  

`[alias]`  
	`graph = log --oneline --graph --decorate`  
	`ls = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate`  
	`ll = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --numstat`  
	`lds = log --pretty=format:"%C(yellow)%h\\ %ad%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --date=short`  
	`conflicts = diff --name-only --diff-filter=U`  
	`local-branches = !git branch -vv | cut -c 3- | awk '$3 !~/\\[/ { print $1 }'`  
	`recent-branches = !git branch --sort=-committerdate | head`  
	`authors = !git log --format='%aN <%aE>' | grep -v 'users.noreply.github.com' | sort -u --ignore-case`
