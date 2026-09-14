---
title: Schema Version
---

## Schema Version

Use schema version 1.1 for single-file authorization models. Modular models use
schema version 1.2 in their `fga.mod` manifest.

**Incorrect (missing schema version):**

```dsl.openfga
model

type user

type document
  relations
    define owner: [user]
```

**Correct (explicit schema version):**

```dsl.openfga
model
  schema 1.1

type user

type document
  relations
    define owner: [user]
```

Schema 1.1 enables conditions, intersection, exclusion, and other advanced features
in a single-file model. See [Modular Models](https://openfga.dev/docs/modeling/modular-models)
for the 1.2 manifest format.
