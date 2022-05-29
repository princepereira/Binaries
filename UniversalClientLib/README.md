# UniversalClientLib
```
This repository contains the binary for universal client.
Universal client act as a client for all message buses (Eg: Nats,Kafka) and NosQL DBS (Eg: Etcd, Redis.).
```
__How to use__:
```

$ wget https://github.com/princepereira/Binaries/raw/main/UniversalClientLib/client
$ chmod +x client
$ ./client -c <Type of server. Eg: Nats/Kafka/Etcd> -a <produce/consume> -i <Server IP> -p <Server Port> -t <Topics/Subjects> -m <PUT/Produce Message>

Producer Eg: ./client -c Nats -a produce -i 127.0.0.1 -p 4222 -t test -m 'Hello World'

Consumer Eg: ./client -c Nats -a consume -i 127.0.0.1 -p 4222 -t "test1,test2"

```
__Bringup Nats for testing the client__:
```
Eg: sudo docker run -d --name nats-server --entrypoint /nats-streaming-server -p 4222:4222 -p 8222:8222 nats-streaming
```
