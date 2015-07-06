# zk-shell

This Docker image contains zk-shell.
It allows usage without python installed.

## Usage

```bash
echo 'ls /' | docker run -i --rm creack/zk-shell zk-shell --run-from-stdin $ZK_HOST:$ZK_PORT
echo 'ls /' | docker run -i --rm --link $ZK_CONTAINER_NAME:zk creack/zk-shell bash -c 'zk-shell --run-from-stdin $ZK_PORT_3888_TCP_ADDR'
```
