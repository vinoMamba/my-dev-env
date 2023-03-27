## go dev env

## how to use

```bash
# clone this repo
git clone git@github.com:vinoMamba/my-dev-env.git -b go-env
# open use vscode
# you need to install vscode extention: Dev Container at first
cd my-dev-env
code .
# reopen in container (ctrl + shift + p -> reopen in container)
```

```json
{
	"name": "Existing Dockerfile",
	"build": {
		"context": "..",
		"dockerfile": "../Dockerfile"
	},
	"mounts": [
		"source=vino-config,target=/root/.config,type=volume",
		"source=vino-repos,target=/root/repos,type=volume",
		"source=vino-vscode,target=/root/.vscode-server/extensions,type=volume",
		"source=vino-go,target=/root/go/bin,type=volume",
		"source=vino-ssh,target=/root/.ssh,type=volume"
	]
}
```
