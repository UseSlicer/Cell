# Config

A simple file is what manages Cell's config. This should be named `config.extension`, where `extension` is essentially any common config file type (e.g. `config.yml`). If an extension isn't passed, [TOML](https://github.com/toml-lang/toml) will be used; however, YAML is used in this manual.

## Example

```yaml
environment: release # Enables verbose logging (debug or release)
http:
  address: ':8080' # The address to bind on
database:
  mongodb: 'mongodb://localhost:27017' # A MongoDB connection string
  redis:
    address: 'localhost:6379' # The Redis instance's address
    password: '' # The Redis password; leave empty if you haven't set one
    db: 0 # The Redis DB to use
sentry:
  dsn: 'https://00000000000000000000000000000000@0000000.ingest.sentry.io/0000000' # The optional Sentry DSN to use
security:
  secret: rh4NaXhju914cn60CHmuMREeQG1Qdh53o4sQ9iZWVlA= # A secure 32 byte key; try `openssl rand -base64 32`
  cert_file: ./some.crt # The optional SSL cert to use
  key_file: ./some.key # The optional SSL key to use
```