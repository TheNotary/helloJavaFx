## Hello Java Fx

This is a demo project showing to to setup a development environment for compiling javaFX applications.  It's from http://docs.oracle.com/javase/8/docs/technotes/guides/deploy/javafx_ant_tasks.html#CHDFHGDE


### Development Environment

Wow... java is apparently in one of those version upgrade transissions.  You need JavaFX which is like... dropped by Oracle at the moment and handed over to the open source community, but is still included in the official java jdk 8 package.  And on linux, the openjfx package is missing in many package repositories so it needs to be compiled from source.  And the source code compilation instructions online are broken due to beign out of date.  I'm not exactly sure if JavaFX is actually a new version of java or if this was a HUGE waste of a day... 

To compile this repo's code, install ant `sudo apt-get install ant` and then download the zip file from oraval's website that includes the jdk 8 [(Java SE... don't ask...)](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).  Be weary of using package maintainers code, there's something odd going on at the moment.  

Once you have the zip file, extract it somewhere... You should try to put it in an expected place like `/usr/lib/jvm/jdk1.8.0_45` otherwise people who download your code and try to compile it will need to do even more work changing the path.  Oh yeah, and in the build.xml, update the line of `<property name="JAVA_HOME" value="/usr/lib/jvm/jdk1.8.0_45"/>` to point to where you thought was close enough.  I think using symlinks and environment variables to specify the proper path might be a good next step but in the meantime there is no official java version manager to take care of this thing for developers.  


### To Build

    $  ant

### To Run

    $  java -jar dist/HelloWorld.jar


