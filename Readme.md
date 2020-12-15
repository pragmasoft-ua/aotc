# Ahead of time compilation example

```
aotc$ javac HelloWorld.java 
aotc$ java HelloWorld 
Hello, World!
aotc$ jaotc --output libHelloWorld.so HelloWorld.class
aotc$ ls -la
total 104
drwxrwxr-x  2 zdv zdv  4096 гру 15 13:32 .
drwxrwxr-x 13 zdv zdv  4096 гру 15 13:31 ..
-rw-rw-r--  1 zdv zdv   427 гру 15 13:32 HelloWorld.class
-rw-rw-r--  1 zdv zdv   114 гру 15 13:32 HelloWorld.java
-rw-rw-r--  1 zdv zdv 86224 гру 15 13:32 libHelloWorld.so
aotc$ java -XX:+UnlockExperimentalVMOptions -XX:AOTLibrary=./libHelloWorld.so HelloWorld
Hello, World!
```
