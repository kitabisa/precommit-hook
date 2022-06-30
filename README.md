# Kitabisa Collection of pre-commit hooks 

## Jira Issue Key on Message Commit
this is a ripoff from [here](https://github.com/avilaton/add-msg-issue-prefix-hook)

We just move the issue key as suffix and in the prefix we add the branch type code

Add this to your `.pre-commit-config.yaml`

```yaml
-   repo: https://github.com/kitabisa/precommit-hook
    rev: v1.0.0  # Use the ref you want to point at
    hooks:
    -   id: add-msg-issue-prefix
```

and install prepare-commit-msg hooks using
```
pre-commit install --hook-type prepare-commit-msg
```

Change how the issue is rendered to the commit message using the `--template` argument.

```yaml
-   repo: https://github.com/avilaton/add-msg-issue-prefix-hook
    rev: v0.0.5  # Use the ref you want to point at
    hooks:
    -   id: add-msg-issue-prefix
        args:
            - --template=[{}] # this will make the issue key surrounded by []

```
