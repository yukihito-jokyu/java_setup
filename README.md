# Introduction

ビルドツールの[Gradle](https://docs.gradle.org/current/userguide/userguide.html)を用いて java のセットアップを行う

# Gradle install

[Homebrew](https://brew.sh/)を用いて Gradle のインストールを行う

```bash
brew install gradle
```

# Setup

以下のコマンドからプロジェクトの初期化をする

```bash
gradle init
```

---

ビルドの種類の選択

```bash
Select type of build to generate:
  1: Application
  2: Library
  3: Gradle plugin
  4: Basic (build structure only)
Enter selection (default: Application) [1..4] 1
```

---

使用するプログラミング言語

```bash
Select implementation language:
  1: Java
  2: Kotlin
  3: Groovy
  4: Scala
  5: C++
  6: Swift
Enter selection (default: Java) [1..6] 1
```

---

Java のバージョン

```bash
Enter target Java version (min: 7, default: 21): 21
```

---

プロジェクト名の設定

```bash
Project name (default: dev): tutorial
```

---

アプリケーションの構造を選択

```bash
Select application structure:
  1: Single application project
  2: Application and library project
Enter selection (default: Single application project) [1..2] 1
```

---

ビルドスクリプトの DSL を選択

```bash
Select build script DSL:
  1: Kotlin
  2: Groovy
Enter selection (default: Kotlin) [1..2] 2
```

---

テストフレームワークを選択

```bash
Select test framework:
  1: JUnit 4
  2: TestNG
  3: Spock
  4: JUnit Jupiter
Enter selection (default: JUnit Jupiter) [1..4] 4
```

---

新しい API や振る舞いを使うか？

```bash
Generate build using new APIs and behavior (some features may change in the next minor release)? (default: no) [yes, no] no
```

---

プロジェクトのセットアップ完了!

```bash
> Task :init
Learn more about Gradle by exploring our Samples at https://docs.gradle.org/8.12.1/samples/sample_building_java_applications.html

BUILD SUCCESSFUL in 3m 46s
1 actionable task: 1 executed
```

---

プロジェクトのファイル構造

```bash
.
├── app
│   ├── build.gradle
│   └── src
│       ├── main
│       │   ├── java
│       │   │   └── org
│       │   │       └── example
│       │   │           └── App.java
│       │   └── resources
│       └── test
│           ├── java
│           │   └── org
│           │       └── example
│           │           └── AppTest.java
│           └── resources
├── gradle
│   ├── libs.versions.toml
│   └── wrapper
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── gradle.properties
├── gradlew
├── gradlew.bat
└── settings.gradle

15 directories, 10 files
```

# Build

以下のコマンドから App.java をビルドする

```bash
./gradlew build
```

# Run

以下のコマンドから App.java を実行する

```bash
./gradlew run
```

実行結果

```bash
Calculating task graph as no cached configuration is available for tasks: run

> Task :app:run
Hello World!

BUILD SUCCESSFUL in 1s
2 actionable tasks: 1 executed, 1 up-to-date
Configuration cache entry stored.
```
