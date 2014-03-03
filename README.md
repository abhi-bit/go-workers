go-worker
============

Grab the code:

```
go get github.com/abhi-bit/go-workers
```

Build the code:

```
go build -o consumer *.go
```

To start the consumer(-n `no. of consumers`):

```
./consumer -n 64
```

To start the producer job(`producing 512 items`):

```
for i in {1..512}; do curl localhost:8000/work -d name=$USER -d delay=$(expr $i % 10)s; done
```
