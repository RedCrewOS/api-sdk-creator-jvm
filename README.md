# api-sdk-creator-jvm

JVM modules to aid developers in the creation of API client SDKs.

See the individual library READMEs for more details.

This is a companion repo for https://github.com/RedCrewOS/api-sdk-creator-mpp

| :memo: | This library is still in active development and may break compatibility in future releases |
|--------|:------------------------------------------------------------------------------------------|

# Development

The repository is managed by [Gradle](https://gradle.org/) with each library being a Gradle module. Each module has
its own version and can be published and consumed independently.

## Building

```shell
$ ./gradlew build
```

## Testing

```shell
$ ./gradlew test
$ cd <project> && ../gradlew test
```

## Publishing & Using

JARs are available via [Jit Pack](https://jitpack.io/#RedCrewOS/api-sdk-creator-mpp). Being a multi-module project,
the module name is part of the identifier for the desired JAR. Jit Pack relies on Git tags to identify new versions, however tagging the whole repo for one module change impacts all modules if the tag was just a version string (eg: `v1.0.0`). Consequently, tags contain the module name, and the module version, so that different modules can be versioned and published separately.

```groovy
dependencies {
  implementation "com.github.RedCrewOS.api-sdk-creator-jvm:ok-http:ok-http_v0.1.0"
}
```
