wetator-maven-plugin
====================

This is a first try to implement a Maven plugin for running Wetator tests.

You can find the Wetator homepage at [http://www.wetator.org/](http://www.wetator.org/).

## Build Status ##
[![Build Status](https://travis-ci.org/fred4jupiter/wetator-maven-plugin.svg?branch=master)](https://travis-ci.org/fred4jupiter/wetator-maven-plugin)

## Usage ##
To use the plugin you have to add this to your Maven pom.xml plugins section:

    <plugin>
	    <groupId>org.wetator</groupId>
	    <artifactId>wetator-maven-plugin</artifactId>
	    <version>1.0.2-SNAPSHOT</version>
	    <configuration>
		    <configFile>src/test/resources/wetator.config</configFile>
		    <testFileDir>src/test/resources/wetator</testFileDir>
	    </configuration>
    </plugin>

By default the plugin includes all *.wet files within the 'testFileDir' folder.

To run the tests run:

    mvn org.wetator:wetator-maven-plugin:execute

## Remarks ##
The wetator-maven-plugin is using the Wetator dependency:

    <dependency>
	    <groupId>org.wetator</groupId>
	    <artifactId>wetator</artifactId>
	    <version>1.0.0</version>
    </dependency>
