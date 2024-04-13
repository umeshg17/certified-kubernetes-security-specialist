#### Documentation Link:

https://github.com/etcd-io/etcd/releases/tag/v3.5.12

#### Pre-Requisite:
```sh
apt-get -y install wget
```
#### Step 1: Create the Base Binaries Directory

```sh
mkdir /root/binaries
cd /root/binaries
```
#### Step 2: Download and Copy the ETCD Binaries to Path
```sh
ETCD_VER=v3.5.12
GITHUB_URL=https://github.com/etcd-io/etcd/releases/download
curl -L ${GITHUB_URL}/${ETCD_VER}/etcd-${ETCD_VER}-linux-amd64.tar.gz -o /tmp/etcd-${ETCD_VER}-linux-amd64.tar.gz
tar xzvf /tmp/etcd-${ETCD_VER}-linux-amd64.tar.gz
cd etcd-${ETCD_VER}-linux-amd64
cp etcd etcdctl /usr/local/bin/
```
#### Step 3: Start ETCD from CLI
```sh
etcd
```

#### Step 4: Verification - Adding and Removing Data to ETCD
```sh
etcdctl put course "cks course is awesome"
```
```sh
etcdctl get course
```
