# Moonrise Labs Renovate Presets

[Renovate](https://docs.renovatebot.com/) configuration presets to to standardize dependency management across repositories with sensible defaults.

## Features

- Automated dependency updates with semantic commits
- Scheduled updates during business hours (9:00-16:00 MT, weekdays)
- Dependency dashboard for visibility
- Lock file maintenance on weekends
- Security vulnerability prioritization
- And more sensible defaults

## Using the Presets

### Basic Usage

Add the following to the `renovate.json` file in your repository:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>moonrise-labs/renovate-config"]
}
```

### Customizing the Configuration

You can extend the base configuration and override specific settings:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>moonrise-labs/renovate-config"],
  "packageRules": [
    {
      "matchPackagePatterns": ["^eslint"],
      "groupName": "eslint packages"
    }
  ]
}
```

## Key Configuration Settings

Our default preset includes the following key settings:

- `branchPrefix`: Uses `feature/` for all Renovate branches
- `dependencyDashboard`: Enabled for better visibility of updates
- `schedule`: Updates run during business hours
- `minimumReleaseAge`: Packages must be at least 3 days old before updating
- `rangeStrategy`: Pin exact versions for consistent builds

## More Information

For more details on Renovate configuration options, see the [Renovate documentation](https://docs.renovatebot.com/).

## Contributing

If you want to suggest changes to these presets, please open a pull request or issue in this repository.