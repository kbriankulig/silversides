# ros-test

Project for ROS development within a Docker container using VSCode.


### Clone the repo

Clone this repository to your local development client (eg. Windows laptop) 

```yaml
       git clone https://github.com/kbriankulig/ros-test.git
```


## Setup VSCode

### Install Local Software

Install the following software packages locally: [Docker Desktop](https://docs.docker.com/engine/install/), [VScode](https://code.visualstudio.com/), and [VSCode Remote Development Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)

### Run an ROS Container in VSCode

This repository contains a `.devcontainer` folder which defines an ROS container configuration for VSCode.  To run this container:

1. Open the Command Pallate `F1` in VSCode
2. Choose: `Dev Container: Open Folder in Container...`
3. Navigate to and select the `ros-test` folder which contains `.devcontainer`
4. Wait about 1 minute for the container to get created.

To see which VSCode extensions are needed for this project and other container settings look at [.devcontainer/devcontainer.json](https://github.com/kbriankulig/ros-test/blob/vscode/.devcontainer/devcontainer.json)


### Confirm Container Setup

To verify the container was setup corretly:

1. Verify the local repo folder `ros-test` was mounted within the container to `/root/ros-test'
2. Verify that `build` and `devel` folders were created within `/root/ros-test/my_ws`



## Development and Testing

### Run a Unit Test

Install the following software packages locally: [Docker Desktop](https://docs.docker.com/engine/install/), [VScode](https://code.visualstudio.com/), and [VSCode Remote Development Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)

### Run an Integration Test

This repository contains a `.devcontainer` folder which defines an ROS container configuration for VSCode.  To run this container:

1. Open the Command Pallate `F1` in VSCode
2. Choose: `Dev Container: Open Folder in Container...`
3. Navigate to and select the `ros-test` folder which contains `.devcontainer`
4. Wait about 1 minute for the container to get created.


### Run a Continuous Integration (CI) Test

To see which VSCode extensions are needed for this project and other container settings look at [.devcontainer/devcontainer.json](https://github.com/kbriankulig/ros-test/blob/vscode/.devcontainer/devcontainer.json)
















### Continuous Integration

The template also comes with basic continuous integration set up. See [`.github/workflows/ros.yaml`](/.github/workflows/ros.yaml).

To remove a linter just delete it's name from this line:

```yaml
      matrix:
          linter: [cppcheck, cpplint, uncrustify, lint_cmake, xmllint, flake8, pep257]
```

## How to use this template

### Prerequisites

You should already have Docker and VSCode with the remote containers plugin installed on your system.

* [Docker Desktop](https://docs.docker.com/engine/install/)
* [VScode](https://code.visualstudio.com/)
* [vscode remote containers plugin](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
* [VSCode Remote Development Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)

### Get the template

Click on "use this template"

![template_use](https://user-images.githubusercontent.com/6098197/91331899-43f23b80-e780-11ea-92c8-b4665ce126f1.png)

### Create your repository

On the next dialog, name the repository you would like to start and decide if you want all of the branches, or just the latest LTS: Foxy.

![template_new](https://user-images.githubusercontent.com/6098197/91332035-713ee980-e780-11ea-81d3-13b170f568b0.png)

Github will then create a new repository with the contents of this one in your account.  It grabs the latest changes as "initial commit".

### Clone your repo

Now you can clone your repo as normal

![template_download](https://user-images.githubusercontent.com/6098197/91332342-e4e0f680-e780-11ea-9525-49b0afa0e4bb.png)

### Open it in vscode

Now that you've cloned your repo onto your computer, you can open it in VSCode (File->Open Folder). 

When you open it for the first time, you should see a little popup that asks you if you would like to open it in a container.  Say yes!

![template_vscode](https://user-images.githubusercontent.com/6098197/91332551-36898100-e781-11ea-9080-729964373719.png)

If you don't see the pop-up, click on the little green square in the bottom left corner, which should bring up the container dialog

![template_vscode_bottom](https://user-images.githubusercontent.com/6098197/91332638-5d47b780-e781-11ea-9fb6-4d134dbfc464.png)

In the dialog, select "Remote Containers: Reopen in container"

VSCode will build the dockerfile inside of `.devcontainer` for you.  If you open a terminal inside VSCode (Terminal->New Terminal), you should see that your username has been changed to `ros`, and the bottom left green corner should say "Dev Container"

![template_container](https://user-images.githubusercontent.com/6098197/91332895-adbf1500-e781-11ea-8afc-7a22a5340d4a.png)


### Update the template with your code

1. Specify the repositories you want to include in your workspace in `src/ros2.repos` or delete `src/ros2.repos` and develop directly within the workspace.
2. If you are using a `ros2.repos` file, import the contents `Terminal->Run Task..->import from workspace file`
2. Install dependencies `Terminal->Run Task..->install dependencies`
3. (optional) Adjust scripts to your liking.  These scripts are used both within tasks and CI.
   1. `setup.sh` The setup commands for your code.  Default to import workspace and install dependencies.
   2. `build.sh` The build commands for your code.  Default to `--merge-install` and `--symlink-install`
   3. `test.sh` The test commands for your code.
4. Develop!