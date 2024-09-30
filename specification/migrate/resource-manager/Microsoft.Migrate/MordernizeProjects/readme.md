# Azure Migrate

> see https://aka.ms/autorest

This is the AutoRest configuration file for Azure Migrate.

---

### Java multi-api

``` yaml $(java) && $(multiapi)
batch:
  - tag: package-migrateengine-2022-05
```

### Tag: package-migrateengine-2022-05 and java

These settings apply only when `--tag=package-migrateengine-2022-05 --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-migrateengine-2022-05' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.azuremigrate.v2022_05_01
  output-folder: $(azure-libraries-for-java-folder)/sdk/azuremigrate/mgmt-v2022_05_01
regenerate-manager: true
generate-interface: true
```

## Getting Started

To build the SDK for Migrate, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`

---

## Configuration

### Basic Information

These are the global settings for the API.

``` yaml
openapi-type: arm
tag: package-migrateengine-2022-05
```

### Tag: package-migrateengine-2022-05

These settings apply only when `--tag=package-migrateengine-2022-05` is specified on the command line.

``` yaml $(tag) == 'package-migrateengine-2022-05'
input-file:
- preview/2022-05-01-preview/migrateEngine.json
```

# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-net-track2
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-python
  - repo: azure-sdk-for-js
  - repo: azure-sdk-for-node
  - repo: azure-resource-manager-schemas
  - repo: azure-powershell
```

## Go

See configuration in [readme.go.md](./readme.go.md)

## Python

See configuration in [readme.python.md](./readme.python.md)