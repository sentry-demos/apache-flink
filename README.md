# sentry-demos/apache-flink

This demo covers integrating Sentry with Apache Flink through a simple WordCount application.

This demo uses `apache-flink` 1.9.0 and log4j

## First Time Setup

Make sure you have Java 8 installed.

It is recommended to use [jenv](https://www.jenv.be/) to manage your Java environment.

Install Apache Maven.

```bash
brew install maven
```

Install [Apache Flink](https://flink.apache.org/downloads.html). An easy way to do this is through homebrew

```bash
brew install flink
```

Add your SENTRY_DSN to the `sentry-properties` file

```properties
dsn=INSERT_DSN_HERE
```

## Run

To compile the jar:

```bash
mvn clean package
```

To run the program:

```bash
# If you installed with homebrew
flink run target/wordcount-0.0.1.jar

# If you downloaded with zip
$FLINK_HOME/bin/flink run target/wordcount-0.0.1.jar
```

You should have errors appear in Sentry.
