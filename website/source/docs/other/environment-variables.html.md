---
description: 'Packer uses a variety of environmental variables.'
layout: docs
page_title: 'Environment Variables - Other'
sidebar_current: 'docs-other-environment-variables'
---

# Environment Variables for Packer

Packer uses a variety of environmental variables. A listing and description of
each can be found below:

-   `PACKER_CACHE_DIR` - The location of the packer cache.

-   `PACKER_CONFIG` - The location of the core configuration file. The format
    of the configuration file is basic JSON. See the [core configuration
    page](/docs/other/core-configuration.html).

-   `PACKER_CONFIG_DIR` - The location of the `.packer.d` config directory

-   `PACKER_LOG` - Setting this to any value other than "" (empty string) or
    "0" will enable the logger. See the [debugging
    page](/docs/other/debugging.html).

-   `PACKER_LOG_PATH` - The location of the log file. Note: `PACKER_LOG` must
    be set for any logging to occur. See the [debugging
    page](/docs/other/debugging.html).

-   `PACKER_NO_COLOR` - Setting this to any value will disable color in the
    terminal.

-   `PACKER_PLUGIN_MAX_PORT` - The maximum port that Packer uses for
    communication with plugins, since plugin communication happens over TCP
    connections on your local host. The default is 25,000. See the [core
    configuration page](/docs/other/core-configuration.html).

-   `PACKER_PLUGIN_MIN_PORT` - The minimum port that Packer uses for
    communication with plugins, since plugin communication happens over TCP
    connections on your local host. The default is 10,000. See the [core
    configuration page](/docs/other/core-configuration.html).

-   `CHECKPOINT_DISABLE` - When Packer is invoked it sometimes calls out to
    [checkpoint.hashicorp.com](https://checkpoint.hashicorp.com/) to look for
    new versions of Packer. If you want to disable this for security or privacy
    reasons, you can set this environment variable to `1`.

-   `TMPDIR` (Unix) / `TMP` `TEMP` `USERPROFILE` (Windows) - The location of
    the directory used for temporary files (defaults to `/tmp` on Linux/Unix
    and `%USERPROFILE%\AppData\Local\Temp` on Windows Vista and above). It
    might be necessary to customize it when working with large files since
    `/tmp` is a memory-backed filesystem in some Linux distributions in which
    case `/var/tmp` might be preferred.
