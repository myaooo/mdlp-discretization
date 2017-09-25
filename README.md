# Minimum Description Length Binning

This is an implementation of Usama Fayyad's entropy based
expert binning method.

Please read the original paper
<a href="http://sci2s.ugr.es/keel/pdf/algorithm/congreso/fayyad1993.pdf">here</a>
for more information.

# Installation and Usage

This code is built using Cython, so you have to run the makefile
in the directory.  First install the requirements with

```
pip install -r requirements.txt
```

and then run

```
make
```

Afterwards, assuming that `discretization.py` and `_mdlp.so` are in the
same directory, you can import the MDLP class.

```
>>> from discretization import MDLP
>>> from sklearn.datasets import load_iris
>>> iris = load_iris()
>>> X = iris.data
>>> y = iris.target
>>> mdlp = MDLP()
>>> conv_X = mdlp.fit_transform(X, y)
```

I recommend creating a virtual environment for this project.

# Tests

To run the unit tests, first install test requirements with

```
pip install -r requirements-test.txt
```

and then run

```
py.test tests/
```

