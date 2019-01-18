[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/beryx/badass-runtime-plugin/blob/master/LICENSE)
[![Build Status](https://img.shields.io/travis/beryx/badass-runtime-plugin/master.svg?label=Build)](https://travis-ci.org/beryx/badass-runtime-plugin)

## Badass Runtime Plugin ##

A Gradle plugin to create custom runtime images for non-modularized applications.

:bulb: For modularized applications use the [Badass-JLink plugin](https://badass-jlink-plugin.beryx.org/releases/latest/).

The plugin offers three tasks: `runtime`, `runtimeZip`, and `suggestModules`.
It also adds an extension with the name `runtime` to let you configure various aspects of its operation.
A simple example configuration is shown below:

```
runtime {
    options = ['--strip-debug', '--compress', '2', '--no-header-files', '--no-man-pages']
    modules = ['java.naming', 'java.xml']
}
```

The following projects illustrate how to use this plugin to create custom runtime images:
- [badass-runtime-example](https://github.com/beryx-gist/badass-runtime-example) - a 'Hello world' application using slf4j and logback.
- [badass-runtime-example-kotlin-tornadofx](https://github.com/beryx-gist/badass-runtime-example-kotlin-tornadofx) - a 'Hello world' application written in Kotlin using [tornadofx](https://github.com/edvin/tornadofx).
- [badass-runtime-spring-petclinic](https://github.com/beryx-gist/badass-runtime-spring-petclinic) - creates a custom runtime image of the [Spring PetClinic](https://github.com/spring-projects/spring-petclinic) application.
- [badass-runtime-pacman](https://github.com/beryx-gist/badass-runtime-pacman) - creates a custom runtime image of Pacman from the [FXGLGames](https://github.com/AlmasB/FXGLGames) repository.


### Please [read the documentation](https://badass-runtime-plugin.beryx.org/releases/latest/) before using this plugin.
