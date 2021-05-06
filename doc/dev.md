
### Dev setup

Clone code in metabase drivers folder.

```
cd /path/to/metabase/modules/drivers

git clone https://github.com/XUJiahua/metabase-impala-driver.git impala
```

Download impala JDBC driver from [Cloudera](https://www.cloudera.com/downloads/connectors/impala/jdbc/2-6-17.html)
to local impala `lib` folder.

```
tree lib

lib
└── ImpalaJDBC42.jar
```

`ImpalaJDBC42.jar` requires JRE 8 and support Impala server 1.0.1 ~ 3.2

![image-20200524093032785](img/image-20200524093032785.png)

Install lib jar into local maven repo.

```
make install-local-jar
```

#### Build Impala Driver

```
cd /path/to/metabase/
bin/build-driver.sh impala
```


