## Server

* Install Ubuntu 18.04.4

* Install git and a few of your favorite admin tools
nano setup/sever_setup.py
sudo apt install python

sudo add-apt-repository ppa:ondrej/php
sudo apt-get update

* Create the `contest` user
    For Ubuntu: `sudo useradd -d /home/contest -m -s /bin/bash contest`
* Switch to contest user: `sudo su contest; cd ~`
* `git clone` the repository inside
* Initialize the git submodules. `git submodule init; git submodule update`
* `sudo python setup/server_setup.py`

    * Leave blank for root mysql password (TODO: Fix this) if there's no mysql installed (change it later after install).
    * p hostname option is used by the apache host setup, do not include port in there.

### Worker
* Install Ubuntu 11.04
* Install git and a few of your favorite admin tools
* Get a root prompt
* Run `curl http://example.com/api_server_setup.php?api_create_key=yourkey|sh`
* Worker takes about 25 minutes to install
* Worker starts processing games when done
