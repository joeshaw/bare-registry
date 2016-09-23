Docker registry without a default storage engine configuration.

Needed because you can't configure a registry using a different
storage engine solely with environment variables.  You encounter a
"multiple storage drivers specified in configuration or environment"
panic.

Based on https://github.com/docker/distribution-library-image but with
the `storage.filesystem` section removed from the `config.yml`.