# Spark

# Sharing Live Code Snippet

https://demo.firepad.io/#d1hHixAQBY


# Reference Repos

Scala Part 
Scala Full https://github.com/nodesense/scala-workshop

Spark Starter https://github.com/nodesense/tesco-spark-july-2021

# Environments

Java 8

```
apt install openjdk-8-jdk curl wget jq -y
```


```
wget https://archive.apache.org/dist/spark/spark-3.0.3/spark-3.0.3-bin-hadoop3.2.tgz

tar xf spark-3.0.3-bin-hadoop3.2.tgz

sudo mv spark-3.0.3-bin-hadoop3.2.tgz /opt

chmod 777 /opt/spark-3.0.3-bin-hadoop3.2.tgz

```

```
nano .bashrc
```

copy paste below config and save file

```


export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
export JRE_HOME=/usr/lib/jvm/java-8-openjdk-amd64 

## Spark Executors

```
spark.conf.set("spark.executor.instances", 4)
spark.conf.set("spark.executor.cores", 4)
```

In above case maximum 16 tasks will be executed at any given time.

other option is dynamic allocation of executors as below -

```
spark.conf.set("spark.dynamicAllocation.enabled", "true")
spark.conf.set("spark.executor.cores", 4)
spark.conf.set("spark.dynamicAllocation.minExecutors","1")
spark.conf.set("spark.dynamicAllocation.maxExecutors","5")
```
This was you can let spark decide on allocating number of executors based on processing and memory requirements for running job.



export SPARK_HOME=/opt/spark-3.0.3-bin-hadoop3.2
export PATH=$PATH:$SPARK_HOME/bin
```


To save, 

Press  Ctrl + O

Press Enter

Press Ctrl  + X   to exit





