# VS Code ROS 2 Workspace Template

This template will get you set up using ROS 2 with VS Code as your IDE.

It's based on [`athackst/vscode_ros2_workspace`](https://github.com/athackst/vscode_ros2_workspace).

## Requirements

**CURRENTLY SUPPORTED ROS 2 VERSION:** Humble Hawksbill

**CURRENTLY SUPPORTED OS:** Ubuntu 22.04

You must also install the following extensions:

* [`C/C++`](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
* [`Python`](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
* [`CMake Tools`](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools)
* [`ROS`](https://marketplace.visualstudio.com/items?itemName=ms-iot.vscode-ros)
* [`ShellCheck`](https://marketplace.visualstudio.com/items?itemName=timonwong.shellcheck)

## Features

### Style

ROS 2-approved formatters are included in the IDE:

* **C++** `uncrustify`, configured from `ament_uncrustify`;
* **Python** `autopep8`, with VS Code settings consistent with the [style guide](https://docs.ros.org/en/humble/The-ROS2-Project/Contributing/Code-Style-Language-Versions.html).

### Tasks

There are many pre-defined tasks, see [`.vscode/tasks.json`](.vscode/tasks.json) for a complete listing.  Feel free to adjust them to suit your needs. They include and automate many common operations such as:

* Creation of packages inside `src/` with proper options, for both `ament_cmake` and `ament_python` build types.
* Building of whole workspaces or sets of packages, with or without debugging support.
* Workspace cleaning.
* Code formatting.

### Workspace organization

`.gitignore` ignores everything but the source code root directory `src/` by default.

All configuration files and VS Code IntelliSense databases can be found in the `.vscode/` folder, which includes a `.gitignore`.

## Configuration

Fork this repository, or copy its contents into yours.

To make it fully work, you have to:

* Edit `.vscode/c_cpp_properties.json` to add include paths from your current workspace and your own system (required for C/C++ software packages).
* Edit `.vscode/settings.json` to add paths from your current Python packages and libraries, both in your workspace and elsewhere, to activate autocomplete and linting features.
