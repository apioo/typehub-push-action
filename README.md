# TypeHub Push Action

This GitHub action submits local TypeAPI/TypeSchema specifications inside your repository to the
[TypeHub platform](https://typehub.cloud/).

## Inputs

## `client_id`

**Required** The typehub.cloud client id, this is either your username or an app key

## `client_secret`

**Required** The typehub.cloud client secret, this is either your password or an app secret

## `directory`

**Required** The directory containing TypeAPI/TypeSchema specifications to TypeHub

## Example usage

```yaml
name: TypeHub
jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: apioo/typehub-push-action@v0.1
        with:
          client_id: '${{ secrets.TYPEHUB_CLIENT_ID }}'
          client_secret: '${{ secrets.TYPEHUB_CLIENT_SECRET }}'
          directory: 'specification'
```
