
This is a backend for TOX (https://github.com/irungentoo/toxcore) for err (http://errbot.net) 2.3.0-rc3 or newer.

As the time of writing the python bindings were not in sync with the core .so.
If you have inconsistencies, try to sync and compile the 2 dependencies at an
earlier date.

## Installation

```
git checkout https://github.com/gbin/err-backend-tox.git
pip install pytox
```

and add:

```
BACKEND = 'TOX'
BOT_EXTRA_BACKEND_DIR = '/path_to/err-backend-tox'
```

to your config.py

## Authentication


```
# You need to set your BOT_IDENTITY in your config.py as this:
BOT_IDENTITY = {
    'username': 'errbot',
}

# You also need to add some bootstrap server so errbot can sync with the swarm.
TOX_BOOTSTRAP_SERVER = ["54.199.139.199", 33445, "7F9C31FE850E97CEFD4C4591DF93FC757C7C12549DDD55F8EEAECC34FE76C029"]

# Bot admins are specified by full crypto TOX hashes.
BOT_ADMINS = ['F9886B47503FB80E6347CC0907D8000144305796DE54693253AA5E574E5E8106C7D002557189', ]
```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D
