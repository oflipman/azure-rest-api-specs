## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: logic
  clear-output-folder: true
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2018-07-preview
  - tag: package-2016-06
  - tag: package-2015-08-preview
  - tag: package-2015-02-preview
```

### Tag: package-2018-07-preview and go

These settings apply only when `--tag=package-2018-07-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2018-07-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/logic/mgmt/package-2018-07-preview/logic
```

### Tag: package-2016-06 and go

These settings apply only when `--tag=package-2016-06 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2016-06' && $(go)
output-folder: $(go-sdk-folder)/services/logic/mgmt/2016-06-01/logic
```

### Tag: package-2015-08-preview and go

These settings apply only when `--tag=package-2015-08-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2015-08-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/logic/mgmt/2015-08-01-preview/logic
```

### Tag: package-2015-02-preview and go

These settings apply only when `--tag=package-2015-02-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2015-02-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/logic/mgmt/2015-02-01-preview/logic
```
