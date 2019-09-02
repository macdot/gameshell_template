## Python Arcade Game Template For GameShell

![screenshot](doc/screenshot.png)

These are instructions on how to get a Python game using the Arcade_ library
working with the GameShell_.

Quick overview:

- Install Python 3.6
- Clone the game from GitHub
- Install link to menu
- Restart

### Install Python 3.6

#### Option 1 - global installation

GameShell runs on Debian Linux. Right now, Debian uses Python 3.5, and Arcade
requires 3.6. So to install 3.6, we need to tell Debian to look at the "testing"
set of files.

Shell over to your GameShell, and copy/paste the following:

```bash
echo "deb http://ftp.fr.debian.org/debian testing main" | sudo tee -a /etc/apt/sources.list
echo 'APT::Default-Release "stable";' | sudo tee -a /etc/apt/apt.conf.d/00local
sudo apt-get update
sudo apt-get -t testing install -y python3.6
```

#### Option 2 - alternative installation, with use of virtual environments

```bash
mkdir -p ~/ini/python
cd ~/ini/python
wget https://www.python.org/ftp/python/3.6.9/Python-3.6.9.tgz
tar fxz Python-3.6.9.tgz
cd Python-3.6.9
./configure         # or ./configure --enable-optimizations
make -j 4
sudo make altinstall
```


### Clone Game

Now clone/grab the code from GitHub and setup virtual environment for Python and Arcade
    
```bash
cd ~/games
git clone https://github.com/pvcraven/gameshell_template.git
python3.6 -m venv venv
source venv/bin/activate && pip install -r requirements.txt
```


### Install the Game

Now we have the code installed, but there is not a link to it from the menu.
Run this command to copy over the link:

```bash
cd ~/games/gameshell_template
chmod u+x install.sh
./install.sh
```


### Reload UI

To make your launcher icon available on GS, run 'Reload UI' option


### Update The Code

Something new on GitHub you want to pull down?

You can update the code with:

```
cd ~/games/gameshell_tempate
git pull
```


### Links

[GameShell](https://www.clockworkpi.com)

[Arcade](http://arcade.academy)
