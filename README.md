# semantic-release-gem

[**semantic-release**](https://github.com/semantic-release/semantic-release) plugin to publish a [gem](https://www.rubygems.org) package.

                                                           |

## Install

```bash
$ npm install semantic-release-gem -D
```

## Usage

The plugin can be configured in the [**semantic-release** configuration file](https://github.com/semantic-release/semantic-release/blob/master/docs/usage/configuration.md#configuration):

```json
{
  "plugins": [
    "@semantic-release/commit-analyzer",
    "@semantic-release/release-notes-generator",
    "semantic-release-gem",
  ]
}
```

## Configuration

### RubyGems registry authentication

The gem authentication configuration is **required** and can be set via [environment variables](#environment-variables).

Only [token](https://docs.npmjs.com/getting-started/working_with_tokens) authentication is supported.

### Environment variables

| Variable       | Description                                                                                                                   |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `RUBYGEM_TOKEN`    | Npm token created via [npm token create](https://docs.npmjs.com/getting-started/working_with_tokens#how-to-create-new-tokens) |

### Options

### RubyGem configuration

### Examples

The `gemPublish` option can be used to skip the publishing to the `RubyGem` registry. For example:

```json
{
  "plugins": [
    "@semantic-release/commit-analyzer",
    "@semantic-release/release-notes-generator",
    ["semantic-release-gem", {
      "npmPublish": false,
      "tarballDir": "dist",
    }]
  ]
}
```
