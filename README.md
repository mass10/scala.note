# scala.note #################################

メモ

# installing sbt on Ubuntu #################################

Ubuntu や Debian-based なディストリビューションでは DEB が提供されているのでこれをインストール。

(参考: http://www.scala-sbt.org/0.13/docs/Installing-sbt-on-Linux.html)

2017年7月3日現在、Scala が Java 9 に対応していないということなので、openjdk-8-jdk をはじめに入れておく↓。

```
$ sudo apt-get install openjdk-8-jdk
```

sbt をインストール↓。

```
$ echo "deb https://dl.bintray.com/sbt/debian /" | sudo tee -a /etc/apt/sources.list.d/sbt.list
$ sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2EE0EA64E40A89B84B2DF73499E82A75642AC823
$ sudo apt-get update
$ sudo apt-get install sbt
```


# sbt でプロジェクトを作成する #################################

```
$ sbt new sbt/scala-seed.g8
```
