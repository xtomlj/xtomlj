# xTomlJ: A Java parser for Tom's Obvious, Minimal Language (TOML)

xTomlJ is a complete [TOML](https://github.com/toml-lang/toml) parser with the
following attributes:

* Supports the latest TOML specification version (1.0.0-rc.1).
* Provides detailed error reporting, including error position.
* Performs error recovery, allowing parsing to continue after an error.

It uses the [ANTLR](https://github.com/antlr/antlr4/) parser-generator and
runtime library.

This is a fork from the original project [TomlJ](https://github.com/tomlj/tomlj).
It was created because the original project appears to be inactive.

## Usage

Parsing is straightforward:

```java
Path source = Paths.get("/path/to/file.toml");
TomlParseResult result = Toml.parse(source);
result.errors().forEach(error -> System.err.println(error.toString()));

String value = result.getString("a. dotted . key");
```

## Getting xTomlJ

xTomlJ is published to Maven Central.

To include using Maven:
```xml
<dependency>
  <groupId>io.github.xtomlj</groupId>
  <artifactId>xtomlj</artifactId>
  <version>1.1.0</version>
</dependency>
```

To include using Gradle: `compile 'io.github.xtomlj:xtomlj:1.1.0'`

## Links

- [GitHub project](https://github.com/xtomlj/xtomlj)
- [Issue tracker: Report a defect or feature request](https://github.com/xtomlj/xtomlj/issues/new)
- [StackOverflow: Ask "how-to" and "why-didn't-it-work" questions](https://stackoverflow.com/questions/ask?tags=tomlj)
