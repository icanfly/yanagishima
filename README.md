# yanagishima

yanagishima is a Web UI for presto like MySQL Workbench.

![yanagishima](screenshot/yanagishima.png)

# Features
* easy to install(no RDBMS)
* easy to use like MySQL Workbench(for example, right click operation)
* query history for self by using local storage
* query bookmark
* show query execution list
* kill running query
* format query
* show columns
* show partitoins
* TSV download by using session storage

# Limitation

* paging results is not supported

# Quick Start
```
wget https://bintray.com/artifact/download/wyukawa/generic/yanagishima-0.0.5.zip
unzip yanagishima-0.0.5.zip
cd yanagishima-0.0.5
vim conf/yanagishima.properties
bin/yanagishima-start.sh
```
see http://localhost:8080/

# Configuration

You need to edit conf/yanagishima.properties.

```
jetty.port=8080 # yanagishima web port
presto.coordinator.server=http://presto.coordinator:8080 # presto coordinator url
select.limit=2000 # if query result exceeds this limit, rest of result is skipped
catalog=hive # presto catalog name
schema=default # presto schema name
user=yanagishima # presto user name
source=yanagishima # presto source name
```

# Start
```
bin/yanagishima-start.sh
```

# Stop
```
bin/yanagishima-stop.sh
```

# Requirements

* Java 8

## Build yanagishima

```
./gradlew distZip
```
