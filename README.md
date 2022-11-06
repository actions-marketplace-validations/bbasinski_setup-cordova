## setup-cordova

[![GitHub Actions](https://img.shields.io/github/workflow/status/bbasinski/setup-cordova/Continuous%20Integration?style=flat-square)](https://github.com/bbasinski/setup-cordova/actions)

Setup your GitHub Actions workflow with Apache Cordova.

**Note: Since this runs in a Linux-based Docker image, Xcode is not available for iOS builds.**

## Example

```yaml
- name: Use bbasinski/setup-cordova
  uses: bbasinski/setup-cordova@0.0.3
  with:
    exec: |
      cordova platform add android && \
      cordova build --no-telemetry && \
      cp "$(find . -name '*.apk')" .
```

## Acknowledgement

Initially based on [coturiv/setup-ionic](https://github.com/coturiv/setup-ionic).

## License

SPDX-License-Identifier: [MIT](LICENSE)
