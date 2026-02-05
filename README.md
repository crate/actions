# Reusable GHA workflows

## CLA-check workflow
The [cla-check](https://github.com/crate/actions/blob/main/.github/workflows/cla-check.yml) workflow
checks if the author of a PR has signed a CLA. The signatures are recorded in the
[cla-check repo](https://github.com/crate/cla-check).

### How to add the CLA-check to a repo
If you want to add this CLA check to a public repo, just copy the
[cla-check.yml](https://github.com/crate/actions/blob/main/.github/workflows/cla-check.yml)
to the repos /.github/workflows/ directory.

### Updating workflow token
**NOTICE**: The action depends on the [REPO_CLABOT_READ_CONTENT_ACCESS org secret](https://github.com/crate/actions/settings/secrets/actions).
This is a PAT that needs refreshed once a year (defined by org policy for create).
We are limited to using these legacy PAT as we have the workflow in one repo (this) and call it from another repo.
See [this discussion](https://github.com/orgs/community/discussions/46566) for why. 
