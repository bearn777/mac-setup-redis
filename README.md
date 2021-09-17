# mac-setup-redis
setup redis on your Mac

type below:

```
brew update
brew install redis
```

To have launchd start redis now and restart at login:
```
brew services start redis
```

to stop it, just run:

```
brew services stop redis
```

Or, if you don't want/need a background service you can just run:

```
redis-server /usr/local/etc/redis.conf
```

Test if Redis server is running.

```
redis-cli ping
```
If it replies “PONG”, then it’s good to go!

Location of Redis configuration file.

```
/usr/local/etc/redis.conf
```

Uninstall Redis and its files.

```
brew uninstall redis
rm ~/Library/LaunchAgents/homebrew.mxcl.redis.plist
```
