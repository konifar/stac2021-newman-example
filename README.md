# stac2021-newman-example

Newman CI example for a presentation on STAC 2021

## Setup

```shell
./scripts/bootstrap
```

## Scenarigo

### Run

```shell
./scripts/scenarigo_run
```

### Structure

```tree.sh
|--.github
|  |--...
|  |--workflows
|  |  |--...
|  |  |--scenarigo-run.yml
|--scenarigo
|  |--environments
|  |  |--prod.env
|  |  |--...
|  |--scenarigo.yaml
|  |--scenarios
|  |  |--include
|  |  |  |--delete_user.yml
|  |  |  |--...
|  |  |--post_v1_users
|  |  |  |--200_success.yml
|--scripts
|  |--...
|  |--scenarigo_run
```

#### environments

- Env variables to run test
- `SCENARIGO_` prefix rule
- They are loaded in `scripts/scenarigo_run`

#### scenarios

- Test scenario xml files
- Common requests are put in include directory
- `{Status Code}_{Scenario name}` naming rule
