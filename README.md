## ipython-notebook Dockerfile

This repository contains a [Dockerfile](https://www.docker.com/)
for [IPython notebook](https://ipython.org/notebook.html) based on [Python](https://docs.python.org)
with numerous additional packages.

### Base Docker Image

* [ubuntu:14.04](https://registry.hub.docker.com/_/ubuntu/)

### Included Packages

* [IPython notebook](https://ipython.org/notebook.html)
* [numpy](http://www.numpy.org/)
* [SciPy](http://www.scipy.org/)
* [Matplotlib](http://matplotlib.org/)
* [SymPy](http://sympy.org)
* [simpy](https://simpy.readthedocs.org)
* [pandas](http://pandas.pydata.org/)
* [patsy](https://patsy.readthedocs.org)
* [scikit-learn](http://scikit-learn.org/)
* [distribute](https://pypi.python.org/pypi/distribute)
* [python-dateutil](http://labix.org/python-dateutil)
* [statsmodels](http://statsmodels.sourceforge.net/)
* [ggplot](https://github.com/yhat/ggplot/)
* [dexy](http://dexy.it/)
* [watchdog](https://github.com/gorakhargosh/watchdog)
* [Pygments](http://pygments.org/)
* [oct2py](https://github.com/blink1073/oct2py)
* [PyBrain](http://pybrain.org/)
* [Natural Language Toolkit](http://www.nltk.org/)
* [Open Computer Vision](http://opencv.org/)

### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [image](https://registry.hub.docker.com/u/fh-wedel/ipython-notebook) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull fhwedel/ipython-notebook`

   (alternatively, you can build an image from the Dockerfile: `docker build -t="fhwedel/ipython-notebook" github.com/fh-wedel/ipython-notebook` or just `make image`)


### Usage

Have your IPython notebooks in the directory `$HOME/notebooks` (start with empty directory), then

    docker run -d -p 8889:8888 -v $HOME/notebooks:/notebooks -e "PASSWORD=ipython" fhwedel/ipython-notebook

Point your browser to https://localhost:8889, login with password *ipython* (as specified above).
