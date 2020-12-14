# X-Toy - Command Line Runner

## Dependencies
- Maven (`sudo apt-get install maven` or `brew install maven`)

## Compilation:
```bash
> mvn clean package  # build the jar
> java -jar target/xtoy-cli.jar example/multiply.toy < example/input.txt # run a file
0006
```

### Note:
The JAR file contained should be platform independent, so you don't actually even need to build this project

## Motivation
As part of [CMU Professor Phillip Compeau's](http://compeau.cbd.cmu.edu/) Programming for Scientists course, the students write [X-Toy](https://lift.cs.princeton.edu/xtoy/index.html) programs using Princeton's Visual X-Toy.  

However, as a TA I need to quickly run their code, which means I don't want to use Visual X-Toy. I tried to find a way to run X-Toy code on the command line, but only found traces of a CLI (`TOY.java`), with all the dependencies missing. Those dependencies were eventually found [here](https://introcs.cs.princeton.edu/java/stdlib/), and so I put together a Maven project instead of following their [incorrect instructions](https://www.cs.princeton.edu/courses/archive/spring12/cos126/checklist/hamming.html) for compiling the source code (there are four dependencies, not simply two).