# ansible-docker

[![Build Status](https://travis-ci.org/nokamoto/ansible-docker.svg?branch=master)](https://travis-ci.org/nokamoto/ansible-docker)

## vagrant
```
vagrant up
ssh -i keys/local admin@192.168.33.21
```

| node | ip |
| --- | --- |
| node1 | 192.168.33.21 |

### RabbitMQ
```
ssh -i keys/local admin@192.168.33.21
sudo docker run -d -p 5672:5672 -p 15672:15672 local/rabbitmq
```

open http://192.168.33.21:15672.

### MariaDB
```
ssh -i keys/local admin@192.168.33.21
sudo docker run -d -p 3306:3306 local/mariadb --wsrep-new-cluster --wsrep_cluster_address=gcomm://
```

```
mysql -u admin -padmin -h 192.168.33.21
```
