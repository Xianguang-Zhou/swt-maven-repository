# swt-maven-repository

Maven repository for SWT and JFace, repository URL: 

	http://xianguang-zhou.github.io/swt-maven-repository/release/

## Usage

1. Set property "swt.artifactId":

```xml
<profiles>
	<profile>
		<id>Linux (x86/GTK)</id>
		<activation>
			<os>
				<name>Linux</name>
				<arch>i386</arch>
			</os>
		</activation>
		<properties>
			<swt.artifactId>org.eclipse.swt.gtk.linux.x86</swt.artifactId>
		</properties>
	</profile>
	<profile>
		<id>Linux (x86_64/GTK)</id>
		<activation>
			<os>
				<name>Linux</name>
				<arch>amd64</arch>
			</os>
		</activation>
		<properties>
			<swt.artifactId>org.eclipse.swt.gtk.linux.x86_64</swt.artifactId>
		</properties>
	</profile>
	<profile>
		<id>Windows (x86)</id>
		<activation>
			<os>
				<family>windows</family>
				<arch>x86</arch>
			</os>
		</activation>
		<properties>
			<swt.artifactId>org.eclipse.swt.win32.win32.x86</swt.artifactId>
		</properties>
	</profile>
	<profile>
		<id>Windows (x86_64)</id>
		<activation>
			<os>
				<family>windows</family>
				<arch>x86_64</arch>
			</os>
		</activation>
		<properties>
			<swt.artifactId>org.eclipse.swt.win32.win32.x86_64</swt.artifactId>
		</properties>
	</profile>
	<profile>
		<id>Mac OS X (x86/Cocoa)</id>
		<activation>
			<os>
				<family>macosx</family>
				<arch>i386</arch>
			</os>
		</activation>
		<properties>
			<swt.artifactId>org.eclipse.swt.cocoa.macosx</swt.artifactId>
		</properties>
	</profile>
	<profile>
		<id>Mac OS X (x86_64/Cocoa)</id>
		<activation>
			<os>
				<family>macosx</family>
				<arch>x86_64</arch>
			</os>
		</activation>
		<properties>
			<swt.artifactId>org.eclipse.swt.cocoa.macosx.x86_64</swt.artifactId>
		</properties>
	</profile>	
</profiles>
```

2. Add SWT Maven repository:

```xml
<repositories>
	<repository>
		<id>swt-repo</id>
		<name>SWT Maven Repository</name>
		<url>http://xianguang-zhou.github.io/swt-maven-repository/release/</url>
	</repository>
</repositories>
```

3. Add SWT Maven dependency:

```xml
<dependencies>
	<dependency>
		<groupId>org.eclipse.swt</groupId>
		<artifactId>${swt.artifactId}</artifactId>
		<version>4.7.1</version>
	</dependency>
</dependencies>
```

