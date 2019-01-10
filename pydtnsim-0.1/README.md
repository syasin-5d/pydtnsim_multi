# NAME

pydtnsim - Python-based DTN simulator

![epidemic.png](http://www.lsnl.jp/~ohsaki/software/pdtnsim/images/epidemic.png)

# DESCRIPTION

**pydtnsim** is a DTN (Delay/Disruption-Tolerant Networking) simulator written
in Python.  Since all programs in **pydtnsim** are written in Python, if you
are a Python programmer, you can easily modify simulator functionalities
and/or add new features.  Python is one of major light-weight programming
languages, which enables rapid prototyping of DTN simulations.  For instance,
when you think of a novel network protocol for DTN, you can rapidly implement
the protocol with the help of high expressiveness of Python language.

Since almost everything in **pydtnsim** is written in Python, **pydtnsim** is
not suitable for extremely large-scale DTN simulations.  For instance,
**pydtnsim** is not suitable for very large-scale DTN simulations with
millions of agents (i.e., mobile nodes/terminals).  However, such limitation
is not an issue in practice since DTN is generally expected to be utilized in
environments with spares agents.

# REQUIREMENTS

- Python version 3.6 or later

- [voronoi program by Steve Fortune](https://netlib.sandia.gov/voronoi/index.html)

# AVAILABILITY

  [http://www.lsnl.jp/~ohsaki/software/pydtnsim/pydtnsim-0.1.tar.gz](http://www.lsnl.jp/~ohsaki/software/pydtnsim/pydtnsim-0.1.tar.gz)

# INSTALLATION

An installatoin program using setuptools module is included in the archive.

An example session is as follows.

    $ pip3 install setuptools
    $ tar xzvf pydtnsim-<VERSION>.tar.gz
    $ cd pydtnsim-<VERSION>.tar.gz
    $ sudo ./setup.py install
    
Then, build and install voronoi program.

    $ mkdir sweep2
    $ cd sweep2
    $ wget https://netlib.sandia.gov/voronoi/sweep2
    $ sh sweep2
    $ wget http://www.lsnl.jp/~ohsaki/software/pydtnsim/sweep2.diff
    $ patch -b <sweep2.diff
    $ make
    $ sudo install -m755 voronoi /usr/local/bin
    
# CONTACT

Hiroyuki Ohsaki (ohsaki[atmark]lsnl.jp)