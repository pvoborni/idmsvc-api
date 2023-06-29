# OpenAPI schema for HMS IDM projects

The OpenAPI schemas are used by the projects

* idm-domains-backend
* idm-domains-frontend
* ipa-hcc

## Integrating submodules with HMS IDM repos

Add submodule to a repository (replace `PATH`)

```
git submodule add https://gitlab.cee.redhat.com/identity-management/idmocp/idm-domains-api.git PATH
```

Update remote changes of a submodule

```
git submodule update --remote
```

then commit the changes. You can manually pull and checkout a revision
to update a submodule to a specific version.

Clone a repository with submodules

```
git clone --recurse-submodules
```

Initialize, fetch, and update submodules of an existing checkout

```
git submodule update --init
```

### Enable submodules in GitLab CI/CD pipeline

Set the environment variable `GIT_SUBMODULE_STRATEGY=normal`, e.g. in CI/CD
variables in the settings menu, see
[CI docs](https://docs.gitlab.com/ee/ci/git_submodules.html).
