# linter-js-yaml

This package will parse your YAML files in Atom through [js-yaml](https://github.com/connec/yaml-js), exposing any issues reported.

## Installation

```
$ apm install linter-js-yaml
```

## Settings

You can configure linter-js-yaml by editing ~/.atom/config.cson (choose Open Your Config in Atom menu) or in Preferences:

```cson
'linter-js-yaml':
  'customTags': [
    "!yaml"
    "!include"
    {
      tag:  "!Base64"
      kind: "mapping"
    }
    {
      tag:  "!Equals"
      kind: "sequence"
    }
    {
      tag: "!If"
      # kind defaults to `scalar`
    }
  ]
```

- `customTags`: List of YAML custom tags. (Default: scalar, unless `kind` is set)
