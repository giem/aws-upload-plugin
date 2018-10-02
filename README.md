# aws-upload-plugin

A [Buildkite](https://buildkite.com/) plugin to upload artifacts to [Amazon S3](https://aws.amazon.com/s3/).

## Example

```yml
steps:
  - name: ":package:"
    command: .ci-scripts/build-and-archive.sh
    plugins:
      aws-upload:
        source-path: ".artifacts/ABC.zip"
        destination-path: "s3:/abc/def/ghi/"
        profile-name: "profile_abc"
```

## Options

### `source-path`

Specifies the local path of the artifact

### `destination-path`

Specifies the S3Uri

### `profile-name`

Specifies the named AWS profile

## License

MPL 2.0 (see [LICENSE](LICENSE))