# To devs

Clone this repo with 

`go get -d github.com/yard-turkey/lib-bucket-provisioner`

**Note** the _vendor/_ directory is ignored and thus not part of this repo.
Library consumers need to use their dep management tool to create the dependencies.

Then install the dependencies

`dep ensure -v`

## Format and Imports

Before merging code into master, be sure to run

```bash
./hack/verify-imports.sh
```

## Update generated code

  NOTE: **ONLY** do this whenever you make changes to the OBC and OB APIs in pkg/apis/objectbucket.io/v1alpha1/*types.go

```bash
./hack/update-codegen.sh
```

# TODO

- P0: solidify and implement the APIs in pkg/apis.  Until we do that, we can't deserialize our workload.
- P1 some basic Reconciler logic to execute the provisioner interfaces passed in
- P2 Robustify!
- P? profit
