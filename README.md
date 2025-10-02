# Built-in Agents

This directory ships Ploinky-ready manifests for infrastructure services that do not
belong to a separate Git repository. They are discovered automatically by the CLI
and can be enabled just like any other agent (for example `enable agent keycloak`).

- `postgres`: Provides a PostgreSQL instance used as the datastore for Keycloak.
- `keycloak`: Runs Keycloak configured for SSO enablement. The manifest declares
  a dependency on the `postgres` agent via its `enable` list.

Manifests here can leverage the extended schema (for example multi-port exposure)
implemented as part of the SSO rollout.
