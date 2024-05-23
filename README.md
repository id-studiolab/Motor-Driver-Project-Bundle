# CIK Project bundle CircuitPython
This repo aims to make a project bundle for the Connected interaction kit

This repo is based on the Adafruit CircuitPython community bundle, this makes it simple and easy to build and distribute the bundle with the help of the github actions.
The repo is made with the help of [this tutorial](https://adafruit-playground.com/u/tyeth/pages/creating-a-circuitpython-library-bundle-for-circup)

To add a remote CircuitPython repo:  
`git submodule add <git url>.git libraries/drivers/<target name>`

To remove a remote CircuitPython repo:  
`git submodule deinit -f libraries/drivers/<target directory>`  
`git rm -f libraries/drivers/<target directory>`

To locally build a bundle:  
`python3 -m venv .env`  
`source .env/bin/activate`  
`pip install circuitpython-build-tools`
`./build.sh`

On every push to this repo it will build and check if all is good  
On every release it will build the .mpy project bundle and add it to the release!