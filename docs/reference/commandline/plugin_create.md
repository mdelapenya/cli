# plugin create

<!---MARKER_GEN_START-->
Create a plugin from a rootfs and configuration. Plugin data directory must contain config.json and rootfs directory.

### Options

| Name         | Type | Default | Description                     |
|:-------------|:-----|:--------|:--------------------------------|
| `--compress` |      |         | Compress the context using gzip |


<!---MARKER_GEN_END-->

## Description

Creates a plugin. Before creating the plugin, prepare the plugin's root
filesystem as well as the [config.json](../../extend/config.md).

## Examples

The following example shows how to create a sample `plugin`.

```console
$ ls -ls /home/pluginDir

total 4
4 -rw-r--r--  1 root root 431 Nov  7 01:40 config.json
0 drwxr-xr-x 19 root root 420 Nov  7 01:40 rootfs

$ docker plugin create plugin /home/pluginDir

plugin

$ docker plugin ls

ID              NAME            DESCRIPTION                  ENABLED
672d8144ec02    plugin:latest   A sample plugin for Docker   false
```

The plugin can subsequently be enabled for local use or pushed to the public registry.

## Related commands

* [plugin disable](plugin_disable.md)
* [plugin enable](plugin_enable.md)
* [plugin inspect](plugin_inspect.md)
* [plugin install](plugin_install.md)
* [plugin ls](plugin_ls.md)
* [plugin push](plugin_push.md)
* [plugin rm](plugin_rm.md)
* [plugin set](plugin_set.md)
* [plugin upgrade](plugin_upgrade.md)
