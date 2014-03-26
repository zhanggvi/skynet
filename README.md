## Build

```
make 'PLATFORM'  # PLATFORM can be linux, macosx, freebsd now
```

## Test

Run these in different console

```
./skynet examples/config	# Launch first skynet node  (Gate server) and a skynet-master (see config for standalone option)
./client 127.0.0.1 8888		# Launch a client, and try to input some words.
```

## About Lua

Skynet push a mondified version of lua 5.2.3 to 3rd/lua , it can share proto type between lua state (http://lua-users.org/lists/lua-l/2014-03/msg00489.html) .

Each lua file only load once and cache it in memory during skynet start, so if you want to reflush the cache , call skynet.cache.clear() .

You can also use the offical lua version , edit the makefile by yourself .

## Blog (in Chinese)

* http://blog.codingnow.com/2012/09/the_design_of_skynet.html
* http://blog.codingnow.com/2012/08/skynet.html
* http://blog.codingnow.com/2012/08/skynet_harbor_rpc.html
* http://blog.codingnow.com/eo/skynet/
