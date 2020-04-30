<p align="center">
  <a href="https://github.com/Sibz/github-status-action"><img alt="github-status-action status" src="https://github.com/Sibz/github-status-action/workflows/test/badge.svg"></a>
</p>

# Github Status Action

Adds a status update to a commit. GitHub will always show the latest state of a context.

## Usage

### Inputs
```yml
 authToken:
    description: 'Use secrets.GITHUB_TOKEN or your own token if you need to trigger other workflows the use "on: status"'
    required: true
  context:
    description: 'The context, this is displayed as the name of the check'
    required: true
  description:
    description: 'Short text explaining the status of the check'
    required: true
  state:
    description: 'The status of the check: success, error, failure or pending'
    required: true
  owner:
    description: 'Repostory onwer, defaults to context github.repository_owner if ommited'
    default: ${{ github.repository_owner }}
  repository:
    description: 'Repository, default to context github.repository if ommited'
    default: ${{ github.repository }}
  sha:
    description: 'SHA of commit to update status on, defaults to context github.sha'
    default: ${{ github.sha }}
  ```
  ### Outputs
  None.
