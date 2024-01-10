INSTALLATION
============

### Get the submodule

```shell
$ git submodule update --init
```

### Install dependencies

```shell
$ sudo apt install libnl-3-dev libnl-cli-3-dev libcap-dev build-essential \
                   python3-pip python3-venv
```

### Prepare python virtenv

```shell
$ python3 -m venv .venv

$ . .venv/bin/activate

(.venv) pip install -r requirements.txt
```

### Build and install `Routing` module

```shell
(.venv) cd Routing/

(.venv) make build-module

(.venv) python setup.py install
```

### Build and install `RplIcmp` module

```shell
(.venv) cd RplIcmp/

(.venv) make lib

(.venv) python setup.py install
```

### Run `simpleRPL`

```shell
(.venv) sudo .venv/bin/python simepleRPL.py [with option]
```

_Note: RPL doesn't work with link local ipv6 address, which start with "fe80::"._