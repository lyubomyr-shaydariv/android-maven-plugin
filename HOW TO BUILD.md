# Prerequisites

Configure JDK 1.8:

```shell
export JAVA_HOME=<JAVA_1.8_SDK_HOME>
export PATH="$JAVA_HOME"/bin:"$PATH"
java -version
```

# Build and install

## Quick build

Run quick build:

```shell
./mvnw -D skipTests=true clean install
```

## Full build

Configure Android SDK:

```shell
export ANDROID_HOME=<ANDROID_SDK_HOME>
"$ANDROID_HOME"/tools/bin/sdkmanager \
  'platforms;android-19' \
  'platforms;android-22' \
  'platforms;android-23' \
  'platforms;android-25' \
  'platforms;android-28' \
  'build-tools;28.0.3' \
  'build-tools;30.0.2'
```

```shell
./mvnw clean install
```
