# tcc-dist

[ ![Download](https://api.bintray.com/packages/miho/TCC/tcc-dist/images/download.svg) ](https://bintray.com/miho/TCC/tcc-dist/_latestVersion)

Bintray distribution infrastructure for TCC

## How to Build tcc-dist

### Requirements

- Java >= 1.8
- Internet connection (dependencies are downloaded automatically)
- IDE: [Gradle](http://www.gradle.org/) Plugin (not necessary for command line usage)
- local TCC executable and C/Header files that shall be added to the distribution

### IDE

Open the `tcc-dist` [Gradle](http://www.gradle.org/) project in your favourite IDE and build it
by calling the `assemble` task.

### Command Line

Navigate to the [Gradle](http://www.gradle.org/) project (e.g., `path/to/tcc-dist`) and enter the following command

#### Bash (Linux/OS X/Cygwin/other Unix-like shell)

    sh gradlew assemble
    
#### Windows (CMD)

    gradlew assemble
    
### Distribution Layout

Distributions layout looks as follows (location of `*.so`- and `*.dll`-files may vary between platforms):
```
.
└── tcc
    └── bin          (on *nix)
        └── tcc
    ├── include
    ├── lib
    ├── tcc.exe      (on Windows)
    ├── *.dll files  (on Windows)
    ├── COPYING
    └── README
            
```
Distributions are are packaged as `tcc.zip`. The locations for distributions are:
```
.
└── src
    └── main
        └── resources
            └── eu
                └── mihosoft
                    └── tcc
                        └── tccdist
                            ├── linux
                            │   |── x64
                            │   |   └── tcc.zip
                            |   └── x86
                            │       └── tcc.zip
                            ├── osx
                            │   └── tcc.zip
                            └── windows
                                |── x64
                                |   └── tcc.zip
                                └── x86
                                    └── tcc.zip
```
