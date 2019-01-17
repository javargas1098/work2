### Create Maven Project
The result of the command ”mvn archetype:generate -B -DgroupId=edu.eci -DartifactId=file-spy”

foto
Parameter basedir: project location
Parameter package: take the compile code and package it in a format.
Parameter groupid: identifies the project
Parameter artifactid: if the name of the jar
Parameter version: project version


The option -B disable the output color.
The option -D define the system properties.
The content of the directory have a pom.xml, and the folders that java create with the parameters
foto

### POM FILES
The word SNAPSHOT means the version of the project that is  in development but the word SNAPSHOT is not important for maven.

Pom packaging is simply a specification that is used to aggregate another project, it’s not a plugin is a phase.

The dependency plugin provides the capability to manipulate artifacts and defines a set of dependencies that the project will fetch from the Maven Repository

**###Dependency Management**

	I add the following dependency (tika-core) in the POM**
	<dependency>
		<groupId>org.apache.tika</groupId>
		<artifactId>tika-core</artifactId>
		<version>1.20</version>
	</dependency>
	then change the App class to FileSpy class and i put the xml code in the POM: 
	<build>
	    <plugins>
    		<plugin>
    			<groupId>org.apache.maven.plugins</groupId>
    			<artifactId>maven-compiler-plugin</artifactId>
    			<configuration>
    				<source>1.8</source>
    				<target>1.8</target>
    			</configuration>
    		</plugin>
    	</plugins>
    </build>
### Building Lifecycles and Plugins
