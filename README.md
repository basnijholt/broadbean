## QCoDeS Pulsebuilder aka broadbean

[![Documentation Status](https://readthedocs.org/projects/broadbean/badge/?version=latest)](http://broadbean.readthedocs.io/en/latest/?badge=latest)

A library for making pulses. Supposed to be used with QCoDeS (in
particular its Tektronix AWG 5014 driver), but works as standalone.

The usage is documented in the jupyter notebooks found in the `docs` folder.

Short description: The broadbean module lets the user compose and
manipulate pulse sequences. The aim of the module is to reduce pulse
building to the logical minimum of specifications so that building and
manipulation become as easy as saying "Gimme a square wave, then a
ramp, then a sine, and then wait for 10 ms" and, in particular, "Do
the same thing again, but now with the sine having twice the frequency
it had before".

The little extra module called `ripasso` performs frequency filtering
and frequency filter  compensation. It could be useful in a general
setting and is therefore factored out to its own module.

The name: The broad bean is one of my favourite pulses.

### Installation

On a good day, installation is as easy as
```
$ git clone https://github.com/QCoDeS/broadbean.git bbdir
$ cd bbdir
$ pip install .
```
behind the scenes, `numpy`, `matplotlib`, and `PyQt5` are installed if
not found.

You can now fire up a python interpreter and go
```
>>> import broadbean as bb
>>> from broadbean import ripasso as rp
```

### Documentation

Apart from the example notebooks, auto-generated documentation is
available.

In the `bbdir` folder, do:
```
$ pip install -r docs_requirements.txt
$ cd docs
$ make html
```
then have a look at the file `bbdir/docs/build/html/index.html`.
