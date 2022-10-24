<h1 align="center"><img src="icon.png"> kubectl-ilog</h1>

<div align="center">
Script to interactively select Deployment|ReplicaSet to print logs produced by containers under the selected resource.
</div>

<br>

# Installation

- Install `kubectl`, `stern`, `jq`, `fzf`.
- Download [`kubectl-ilog`](./kubectl-ilog) and save somewhere under the `$PATH` as executable file.

# Usage

```sh
kubectl-ilog

Print container logs of selected deployment or replicaset.

Usage:
 kubectl-ilog
 kubectl-ilog -h
 kubectl-ilog -r
 kubectl-ilog -s 15m
 kubectl-ilog -r -s 15m

Options:
  -s duration       Return logs newer than a relative duration like 5s, 2m, or 3h. Default: 30m
  -r kind           Use replicasets to select resource. Default: deployment
  -h help           Prints this help

Dependencies:

 - stern: https://github.com/stern/stern
 - kubectl: https://kubernetes.io/docs/tasks/tools/install-kubectl/
 - jq: https://stedolan.github.io/jq/download/
 - fzf: https://github.com/junegunn/fzf
 - awk
```