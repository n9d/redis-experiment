# redis実験環境

- `docker-compose run srv bash`


- `redis-cli -h redis incr mycounter`
- `redis-cli -h redis decr mycounter`


## monitor

```
$ docker-compose run srv redis-cli -h redis monitor
Creating client_srv_run ... done
OK
1626218187.774000 [0 192.168.48.4:54626] "incr" "mycounter"
1626218189.872309 [0 192.168.48.4:54636] "incr" "mycounter"
1626218211.414861 [0 192.168.48.4:54646] "incr" "mycounter"
```

- 他のターミナルから `docker-compose run srv redis-cli -h redis incr mycounter` 等を実行する
