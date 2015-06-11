# Internship

## Setting up your environment

* Add the following lines to your ~/.bashrc (once and for all)

```bash
# Use my libraries and binaries
export BREDIN=/people/bredin/install
export PATH=$BREDIN/bin:$PATH
export LD_LIBRARY_PATH=$BREDIN/lib64:$BREDIN/lib:$LD_LIBRARY_PATH
export PKG_CONFIG_PATH=$BREDIN/lib/pkgconfig:$BREDIN/lib64/pkgconfig:$PKG_CONFIG_PATH

# Python virtualenv (http://virtualenv.pypa.io/)
export PIP_REQUIRE_VIRTUALENV=true
export WORKON_HOME=/people/`whoami`/pyenv
mkdir -p $WORKON_HOME
source $BREDIN/bin/virtualenvwrapper.sh
```

* Create a Python isolated environment and install several useful tools

```bash
$ export NEW_ENV=internship
$ mkvirtualenv $NEW_ENV
$ pip install "ipython[notebook]"
$ pip install numpy
$ pip install scipy
$ pip install matplotlib
$ ln -s $BREDIN/lib/python2.7/site-packages/cv2.so $WORKON_HOME/$NEW_ENV/lib/python2.7/site-packages/cv2.so
$ ln -s $BREDIN/lib/python2.7/site-packages/cv.py $WORKON_HOME/$NEW_ENV/lib/python2.7/site-packages/cv.py
```

## Getting started 

```bash
$ workon internship
$ git clone https://github.com/hbredin/ke.git $HOME/internship; 
$ cd $HOME/internship/notebooks
$ ipython notebook
```
