# gnmi-python-tutorial
Quick gNMI Python tutorial

## Installation
```bash
git clone --recursive https://github.com/remingtonc/gnmi-python-tutorial
# Use your favorite Python dep handling
# with requirements.txt, or with pipenv...
pipenv install
```

## YANG
We're using `pyang` to parse the YANG modules and determine what data we want to use in gNMI.

```bash
cd industry-models/vendor/cisco/xr/701
# Let's say we want openconfig-interfaces...
pyang -f tree openconfig-interfaces.yang openconfig-if*.yang
```

## gNMI
We're using [`cisco-gnmi`](https://pypi.org/project/cisco-gnmi/) ([`cisco-ie/cisco-gnmi-python`](https://github.com/cisco-ie/cisco-gnmi-python)) - the class documentation and README in the repository has usage details.

```bash
(gnmi-python-tutorial) [gnmi-python-tutorial] python
Python 3.7.5 (default, Nov  1 2019, 02:16:32)
[Clang 11.0.0 (clang-1100.0.33.8)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> from cisco_gnmi import ClientBuilder
>>>
```