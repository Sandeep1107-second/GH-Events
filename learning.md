# Acitvity Types and Filter

## Activity types -
```
on:                
  pull_request:      -> Event
    types:
      - opened       -> Run on opened PR
  workflow_dispatch: -> manually run the workflows

```
- We can add types on some Events to get better control of the workflows
- pull-request has many types **opened, closed, edited etc.**


## Filters

```
on:
  push:
    branches:
      - main
      - 'dev-*'  -> branches starts with dev..
      - 'feat/**'

```
- Workflows will run when a push is made to a **main** branch.
- This gives more control over code pushed to the Repo.
- ``'feat/**'`` This means that branch name starts with **feat/** will be triggered.

- `*` (Single asterisk) Doesn't allow furthur slashes in the branch name.

- `**` is used to allow furthur slashes in the branch name