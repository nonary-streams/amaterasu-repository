# Amaterasu Core package repository

This repository distributes signed [Amaterasu](https://github.com/nonary-streams/amaterasu) Core sets and independently installable native plugins.

For the Linux x86-64 feed, open **Modules → Repositories → Add repository** in the Amaterasu console and use the following enrollment details. Confirm the fingerprint against the [Amaterasu publishing guide](https://github.com/nonary-streams/amaterasu/blob/main/docs/repository-publishing.md) before enrolling.

```json
{"id":"amaterasu","location":"https://raw.githubusercontent.com/nonary-streams/amaterasu-repository/catalog/linux-x86_64","public_key":"6c399560a1dbe4b646d3be60344fa114d05cdcd7b567a3648958aa1818805b00"}
```

Publisher fingerprint `e89ff0faa32cd120fa58642edff3c0f3e118c9d1099e302b1234dd33870c706c`.

The first Core set is built from Amaterasu revision `6a97a8c5` and its pinned dependencies on CachyOS. The package includes the plugin installation coordinator and was checked with an isolated Linux startup and retirement probe. The Linux package does not include the NVIDIA RTX HDR runtime. The current catalog targets Linux x86-64.

When publishing a plugin, keep the Core set in the catalog and add a `--plugin PLUGIN_ID IMPLEMENTATION PACKAGE` entry. The host verifies the plugin signature, dependency versions and authorized grants before activation. See [Plugin packages and driver setup](https://github.com/nonary-streams/amaterasu/blob/main/docs/plugin-driver-installation.md) for package details.
