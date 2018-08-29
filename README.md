Gradle Test

```bash
$ gradle init --type java-application
Starting a Gradle Daemon (subsequent builds will be faster)

BUILD SUCCESSFUL in 3s
2 actionable tasks: 2 executed

$ ll
total 40
drwxr-xr-x  9 sskim  staff   288 Aug 30 08:12 .
drwxr-xr-x  4 sskim  staff   128 Aug 30 08:11 ..
drwxr-xr-x  4 sskim  staff   128 Aug 30 08:12 .gradle
-rw-r--r--  1 sskim  staff   993 Aug 30 08:12 build.gradle
drwxr-xr-x  3 sskim  staff    96 Aug 30 08:12 gradle
-rwxr-xr-x  1 sskim  staff  5296 Aug 30 08:12 gradlew
-rw-r--r--  1 sskim  staff  2260 Aug 30 08:12 gradlew.bat
-rw-r--r--  1 sskim  staff   359 Aug 30 08:12 settings.gradle
drwxr-xr-x  4 sskim  staff   128 Aug 30 08:12 src

$ gradle compileJava

BUILD SUCCESSFUL in 8s
1 actionable task: 1 executed

$ ll
total 40
drwxr-xr-x  10 sskim  staff   320 Aug 30 08:14 .
drwxr-xr-x   4 sskim  staff   128 Aug 30 08:11 ..
drwxr-xr-x   5 sskim  staff   160 Aug 30 08:14 .gradle
drwxr-xr-x   4 sskim  staff   128 Aug 30 08:14 build
-rw-r--r--   1 sskim  staff   993 Aug 30 08:12 build.gradle
drwxr-xr-x   3 sskim  staff    96 Aug 30 08:12 gradle
-rwxr-xr-x   1 sskim  staff  5296 Aug 30 08:12 gradlew
-rw-r--r--   1 sskim  staff  2260 Aug 30 08:12 gradlew.bat
-rw-r--r--   1 sskim  staff   359 Aug 30 08:12 settings.gradle
drwxr-xr-x   4 sskim  staff   128 Aug 30 08:12 src

$ gradle run

> Task :run
Hello world.

BUILD SUCCESSFUL in 0s
2 actionable tasks: 1 executed, 1 up-to-date

$ gradle jar

BUILD SUCCESSFUL in 0s
2 actionable tasks: 1 executed, 1 up-to-date
      
$ tree
.
|-- build
|   |-- classes
|   |   `-- java
|   |       `-- main
|   |           `-- App.class
|   |-- libs
|   |   `-- gradle_test.jar
|   `-- tmp
|       |-- compileJava
|       `-- jar
|           `-- MANIFEST.MF
|-- build.gradle
|-- gradle
|   `-- wrapper
|       |-- gradle-wrapper.jar
|       `-- gradle-wrapper.properties
|-- gradlew
|-- gradlew.bat
|-- settings.gradle
`-- src
    |-- main
    |   `-- java
    |       `-- App.java
    `-- test
        `-- java
            `-- AppTest.java

15 directories, 11 files
```

```bash
$ git init
Initialized empty Git repository in /Users/sskim/sskim.study/java/gradle_test/.git/
$ echo "Gradle Test" > README.md       
$ ll
total 48
drwxr-xr-x  12 sskim  staff   384 Aug 30 08:25 .
drwxr-xr-x   4 sskim  staff   128 Aug 30 08:11 ..
drwxr-xr-x   9 sskim  staff   288 Aug 30 08:24 .git
drwxr-xr-x   5 sskim  staff   160 Aug 30 08:14 .gradle
-rw-r--r--   1 sskim  staff    12 Aug 30 08:25 README.md
drwxr-xr-x   5 sskim  staff   160 Aug 30 08:15 build
-rw-r--r--   1 sskim  staff   993 Aug 30 08:12 build.gradle
drwxr-xr-x   3 sskim  staff    96 Aug 30 08:12 gradle
-rwxr-xr-x   1 sskim  staff  5296 Aug 30 08:12 gradlew
-rw-r--r--   1 sskim  staff  2260 Aug 30 08:12 gradlew.bat
-rw-r--r--   1 sskim  staff   359 Aug 30 08:12 settings.gradle
drwxr-xr-x   4 sskim  staff   128 Aug 30 08:12 src
$ git add .
$ git commit -m "init"
[master (root-commit) 547c557] init
 Committer: sskim <sskim@sskimui-MacBook-Pro.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 26 files changed, 333 insertions(+)
 create mode 100644 .gradle/4.10/fileChanges/last-build.bin
 create mode 100644 .gradle/4.10/fileContent/fileContent.lock
 create mode 100644 .gradle/4.10/fileHashes/fileHashes.bin
 create mode 100644 .gradle/4.10/fileHashes/fileHashes.lock
 create mode 100644 .gradle/4.10/gc.properties
 create mode 100644 .gradle/4.10/javaCompile/classAnalysis.bin
 create mode 100644 .gradle/4.10/javaCompile/javaCompile.lock
 create mode 100644 .gradle/4.10/javaCompile/taskHistory.bin
 create mode 100644 .gradle/4.10/taskHistory/taskHistory.bin
 create mode 100644 .gradle/4.10/taskHistory/taskHistory.lock
 create mode 100644 .gradle/buildOutputCleanup/buildOutputCleanup.lock
 create mode 100644 .gradle/buildOutputCleanup/cache.properties
 create mode 100644 .gradle/buildOutputCleanup/outputFiles.bin
 create mode 100644 .gradle/vcs-1/gc.properties
 create mode 100644 README.md
 create mode 100644 build.gradle
 create mode 100644 build/classes/java/main/App.class
 create mode 100644 build/libs/gradle_test.jar
 create mode 100644 build/tmp/jar/MANIFEST.MF
 create mode 100644 gradle/wrapper/gradle-wrapper.jar
 create mode 100644 gradle/wrapper/gradle-wrapper.properties
 create mode 100755 gradlew
 create mode 100644 gradlew.bat
 create mode 100644 settings.gradle
 create mode 100644 src/main/java/App.java
 create mode 100644 src/test/java/AppTest.java
$ git remote add origin https://github.com/sooyaa/study-java-gradle_test.git
$ git push -u origin master 
Username for 'https://github.com': sooyaa
Password for 'https://sooyaa@github.com': 
Counting objects: 50, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (27/27), done.
Writing objects: 100% (50/50), 152.75 KiB | 6.94 MiB/s, done.
Total 50 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), done.
To https://github.com/sooyaa/study-java-gradle_test.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
```
