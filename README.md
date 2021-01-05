# Environment data parser

Parses through all environmental data collected throughout Season 10 and Season 11. This software is a GUI used for observing environmental data.


## Hardware Requirements

- Internet connection
- Display screen

## Software Requirements

- iRODS account
- Docker
- Linux/Ubuntu system or
- MacOS system or
- Windows 10 with WSL2 (Windows 10 Home not supported)

## Executing the parser

### Linux/Ubuntu

- Open terminal
- Execute `xhost +local:root`
- Execute with `docker run -it --rm --env="DISPLAY" --env="QT_X11_NO_MITSHM=1" --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" phytooracle/env_parser`
- Execute `xhost -local:root` once finished

### MacOS

- Make sure to have XQuarz installed
- Navigate to the XQuarz settings and activate the option "Allow connections from network clients"
- Open terminal
- Execute `xhost +local:root` OR `xhost + 127.0.0.1`
- Execute with `docker run -e DISPLAY=host.docker.internal:0 phytooracle/env_parser`
- Execute `xhost -local:root` OR `xhost - 127.0.0.1` once finished

### Windows 10 with WSL2

- Make sure to be able to execute X11 (refer to [this article](https://virtualizationreview.com/articles/2017/02/08/graphical-programs-on-windows-subsystem-on-linux.aspx) for links on installing X11 on Windows 10)
- Access Linux subsystem
- Execute `xhost +local:root`
- Execute with `docker run -it --rm --env="DISPLAY" --env="QT_X11_NO_MITSHM=1" --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" phytooracle/env_parser`
- Execute `xhost -local:root` once finished

## Instructions

This is the Environmental parser for the gantry scanalyzer data. Please select the season and day you are interested in viewing and select "prep data"; This will ensure data is downloaded and uncompressed. Please give up to 10 minutes to donwload and uncompress your data, depending on your internet connection. When data is ready, press "load data", please wait up to 1-2 minutes. Once loaded choose "day median" to view median of all collected environmental variables. If you are interested in a specific data at a specific time, select which environmental variable you are interested in and press "show graph". Please keep in mind that the data might take a moment to load. Thank you for using the Environmental parser.

