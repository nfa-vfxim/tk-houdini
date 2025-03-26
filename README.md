[![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/nfa-vfxim/tk-houdini?include_prereleases)](https://github.com/nfa-vfxim/tk-houdini) 
[![GitHub issues](https://img.shields.io/github/issues/nfa-vfxim/tk-houdini)](https://github.com/nfa-vfxim/tk-houdini/issues) 
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

# initial commit
# ShotGrid Engine for Houdini <img src="icon_256.png" alt="Icon" height="24"/>

ShotGrid Pipeline Toolkit integration in Houdini

## Requirements

| ShotGrid version | Core version | Engine version |
|------------------|--------------|----------------|
| -                | v0.20.5      | -              |

**ShotGrid fields:** -

**Frameworks:** -

## Configuration

### Booleans

| Name                       | Description                                                                                                                                                                                                                                                                             | Default value |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| `automatic_context_switch` | Controls whether toolkit should attempt to automatically adjust its context every time the currently loaded file changes. Defaults to True.                                                                                                                                             | True          |
| `enable_sg_menu`           | Controls whether a menu will be built with commands registered by the installed apps. It is not currently possible to rebuild the menu on a ShotGrid context switch, so this option allows for the menu to be disabled in favor of the ShotGrid shelf which can be rebuilt dynamically. | True          |
| `enable_sg_shelf`          | Controls whether a shelf will be built with commands registered by the installed apps. The shelf will be rebuilt dynamically as the ShotGrid context changes.                                                                                                                           | True          |
| `debug_logging`            | Controls whether debug messages should be emitted to the logger                                                                                                                                                                                                                         | False         |


### Lists

| Name                     | Description                                                                                                                                                                                                                                                                                                                                                                                                               | Default value                |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| `menu_favourites`        | Controls the favourites section on the main menu. This is a list and each menu item is a dictionary with keys app_instance and name. The app_instance parameter connects this entry to a particular app instance defined in the environment configuration file. The name is a menu name to make a favourite.                                                                                                              |                              |
| `launch_builtin_plugins` | Comma-separated list of tk-houdini plugins to load when launching Houdini. Use of this feature disables the classic mechanism for bootstrapping Toolkit when Houdini is launched.                                                                                                                                                                                                                                         | []                           |
| `run_at_startup`         | Controls what apps will run on startup.  This is a list where each element is a dictionary with two keys: 'app_instance' and 'name'.  The app_instance value connects this entry to a particular app instance defined in the environment configuration file.  The name is the menu name of the command to run when the Houdini engine starts up. If name is '' then all commands from the given app instance are started. | []                           |
| `review_field_matches`   | Matches for the review template field value to enable "Submit for Review".                                                                                                                                                                                                                                                                                                                                                | ['main', 'beauty', 'master'] |


### Strings

| Name           | Description                                                                               | Default value |
|----------------|-------------------------------------------------------------------------------------------|---------------|
| `review_field` | Template field to match for enabling "Submit for Review" when publishing image sequences. |               |


