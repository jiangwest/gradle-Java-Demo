# gradle-Java-Demo
how to use Gradle to build and run Java

a very simple example to illustrate one miss of most examples.


> 注意 *java的源码目录默认值*，否则容易出错
> 网上大多示例并没指出此点

- 更改gradle默认目录: `sourceSets` 
  - e.g.: 当前目录表示为 -> srcDir '.'
    
    
build.gradle 示例  

```Gradle
sourceSets {
    main {
        java {
            srcDir 'src/java' // 指定源码目录
        }
        resources {
            srcDir 'src/resources' //资源目录
        }
    }
}
```


- for java: 主类名与其文件名一致，否则出错
  - e.g., 主类名为 `class HelloGradle`，则其文件名必须为`HelloGradle.java`
    - 并与build.gradle文件中 `mainClassName = 'HelloGradle` 相对应
