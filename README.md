# 30-under-30
30 of my favorite packages/utilities/aliases under 30MB in size :)

## Network
### Prettyping (https://github.com/denilsonsa/prettyping)
A prettier `ping`.
```
prettyping --nolegend google.com
```

## System
### ncdu (https://formulae.brew.sh/formula/ncdu)
A better `du`.
```
ncdu --color dark -rr -x --exclude .git --exclude node_modules
```

## Sharing
### Seashells (https://seashells.io/)
Allows you to pipe terminal output to a web session. Helpful for sharing command output, monitoring status on the go, you get the idea.
```
htop | seashells --delay 5
```

## Aliases
### Kubectl Aliases (https://github.com/ahmetb/kubectl-aliases)
Takes some getting used to, but you won't know how you survived without them after you do.
```
kgpo
ksysgpo
kgdep
```

### Personal Aliases and Functions
#### Kubernetes
##### shell
Open up a bash shell in the current cluster.
```
alias shell="kubectl run my-shell --rm -i --tty --image ubuntu -- bash"
```

#### Python
##### simpleserver
Bring up a simple webserver
```
alias simpleserver="python3 -m http.server"
```
##### pipsave
Download a package from PyPi and write the dependency to the requirements.txt in the current folder.

```
function pipsave() {
  pip install $1 && pip freeze | grep $1 >> requirements.txt
}
```
