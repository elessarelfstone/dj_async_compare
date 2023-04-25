# dj_async_compare

Just a simple example of async(aiohttp) and sync(Django) servers. 

## Run servers

For aiohttp:
```bash
python ./servers/aio/server.py
```

For Django:
```bash
python ./servers/dj/manage.py runserver
```


## Benchmarks

Download Apache binaries from [here](https://www.apachelounge.com/download/), unpack and add to PATH variable.
Now you you'll able run _ab_ utility. 

For example, to show how many requests per second Django server is capable of serving:

```bash
ab -n 1000 -c 10 http://127.0.0.1:8000/
```

and aiohttp:

```bash
ab -n 1000 -c 10 http://127.0.0.1:8088/
```

Play around with -c parameter increasing for each server.