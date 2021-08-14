# ex-redis
redis module for exercise


Compile:
```shell
make
```



Using Module:
add path of ex.so module to redis configuration file
```
loadmodule /path/to/ex.so
```

Or from redis-cli

```
MODULE LOAD /path/to/ex.so
```


How to use this module:

* `EX.HINCRBYFLOAT`: same as HINCRBYFLOAT but stored as fixed floating point.

```
HSET foo a 5000
(integer) 0
HGETALL foo
1) "a"
2) "5000"
EX.HINCRBYFLOAT foo a -0.23
"4999.77"
```
