# markdown-mermaid-tests

## gitGraph change of default branch name

```mermaid
%%{init: { 'gitGraph': {'mainBranchName': 'master'}} }%%
gitGraph
    commit
    branch production
    checkout master
    commit id: "Michael builds a node"
    branch 01_newfeature
    checkout 01_newfeature
    commit id: "Helen adds a feature"
    checkout master
    commit id: "Michael builds another node"
    commit id: "Iain builds a node"
    checkout 01_newfeature
    commit id: "Helen adds more of the feature"
    checkout master
    merge 01_newfeature id: "Helen merges the feature in"
    commit id: "Chris builds a node"
    commit id: "Michael builds yet another node"
    checkout production
    merge master id: "Helen merges to production"
```
