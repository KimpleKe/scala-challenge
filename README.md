# yow 2013
## Introduction to FP in Scala

This is the base project for the workshop.

__note__: please test your environment before you arrive so we can get
started quickly on the day.

### Core

The `core` package contains no coding exercise, but provides a set
of useful abstractions that we will build on top of as we progress.
It is not necessary to study these in detail, but it may be useful
to keep this package in mind when implementing some of other challenges.


## The Challenges

## Warmup

We will use the list exercises to introduce some basic FP concepts
and scala syntax.

### Challenge 1

Implement the missing methods from the Result data type.


### Challenge 2

Implement the Reader data type.


### Challenge 3

Implement the Writer data type.


### Challenge 4

Implement the State data type.


### Challenge 5

Implement the ReaderT data type.


### Challenge 6

Implement the WriterT data type.


### Challenge 7

Implement the StateT data type.


### Challenge 8

This challenge presents two styles in 8a and 8b.

8a uses a function to encode reader/writer/state/result for a Http data type.

8b uses a transformer stack to encode reader/writer/state/result for a Http data type.


### Challenge 9

The 9th and final challenge is to implement test and runtime interpretters for the Http
stack in challenge 8.


## Working with the code.

 - Challenges are in roughly increasing difficulty.

 - Challenges can be done in any order (except 8b which depends on  5, 6, 7.

 - There is a branch that answers each challenge. If you want to skip
   a challenge (for example, you wanted to do 7 and 8b, you can merge
   in the answers for the other exercises with:

```
git merge origin/challenge5
git merge origin/challenge6
```

 - If you want to have a sneak peek you can just do a diff:

```
git diff origin/challenge2 src/main/scala/challenge2
```


## Getting started

Before you attend you will need to get a few things
ready and ensure everything is setup properly. `sbt`
is going to do all the heavy lifting though, so
hopefully it is all straight forward, if not, send
us an email via <mark@hibberd.id.au>.


Pre requisuites.

 1. A valid install of java 6+
 2. git
 3. **if you are windows only** install sbt using the [msi installer](http://scalasbt.artifactoryonline.com/scalasbt/sbt-native-packages/org/scala-sbt/sbt/0.13.0/sbt.msi)


Getting scala and validating your environment (for unix):

    git clone https://github.com/markhibberd/yow-patterns-in-types.git
    cd yow-patterns-in-types
    ./sbt test:compile


Getting scala and validating your environment (for windows):

    git clone https://github.com/markhibberd/yow-patterns-in-types.git
    cd yow-patterns-in-types
    sbt test:compile


For either platform this may take a few minutes. It will:

 1. Download the sbt build tool.
 2. Download the required versions of scala.
 3. Compile the main and test source code.
 4. Run the tests.


You should see green output, no errors and, an exit code of 0.


## Working with scala.

Any good text editor will be sufficient for the course. If you
prefer an IDE, you can use the eclipse based scala-ide or
intellij with the scala and sbt plugins installed.

You can generate project files for intellij with:

    ./sbt 'gen-idea no-classifiers'

You can generate project files for eclipse with:

    ./sbt eclipse

Just note that if you choose eclipse or intellij, have a
backup texteditor as well, because there won't be enough
time to debug any editor issues.
