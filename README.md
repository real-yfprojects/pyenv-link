# pyenv-link
A [pyenv](https://github.com/pyenv/pyenv) plugin for linking python versions and virtual envs into your pyenv root.

This plugin recommends the [pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv/) plugin.

## Installation

This will install the latest development version of *pyenv-link* into
the `$(pyenv root)/plugins/pyenv-link` directory.

**Important note:**  If you installed pyenv into a non-standard directory, make
sure that you clone this repo into the 'plugins' directory of wherever you
installed into.

From inside that directory you can:
 - Check out a specific release tag.
 - Get the latest development release by running `git pull` to download the
   latest changes.


```bash
git clone https://github.com/real-yfprojects/pyenv-link.git $(pyenv root)/plugins/pyenv-link
```

For the Fish shell:

```fish
git clone https://github.com/real-yfprojects/pyenv-link.git (pyenv root)/plugins/pyenv-link
```

## Usage

Make an arbitrary virtualenv available through pyenv. This automatically guesses a fitting name from the prompt, the directory name or the location of the venv.

```console
$ pyenv link version .venv
Linked new version named myproject-py3.10
```

You can also specify a name to use for the venv.

```console
$ pyenv link version .venv myname
Linked new version named myname
```

Now you can make pyenv activate/use the venv automatically:

```console
$ pyenv local myproject-py3.10
```

## Contributing
This project is developed in an open-source, community-driven way, as a voluntary effort in the authors’ free time.

All kinds of contributions are greatly appreciated. This not only includes implementing new features but also refactoring work or improvements to the documentation.
Bug reports, feature requests and other suggestions are welcome too.

### TODO

- [ ] Tests
- [ ] CI