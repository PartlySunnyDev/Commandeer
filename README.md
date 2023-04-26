# Commandeer
[![](https://jitpack.io/v/PartlySunnyDev/Commandeer.svg)](https://jitpack.io/#PartlySunnyDev/Commandeer)
![](https://img.shields.io/github/languages/top/PartlySunnyDev/Commandeer)
![](https://img.shields.io/github/v/release/PartlySunnyDev/Commandeer)
![](https://img.shields.io/github/stars/PartlySunnyDev/Commandeer?style=social)

## Easy to use annotation based command framework for Spigot
This project is quite similar to ACF, so mostly this is for personal use. Feel free to use it though.

### Features
- [x] Annotation based commands
- [x] Powerful command argument system
- [x] Simple command registration and completion

### Setup
1. Add the jitpack repository to your pom.xml
```xml
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url> <!-- Add this repository -->
    </repository>
</repositories>
```

2. Add the dependency to your pom.xml
```xml
<dependencies>
    <dependency>
        <groupId>com.github.PartlySunnyDev</groupId>
        <artifactId>Commandeer</artifactId>
        <version>1.0</version> <!-- Add this dependency -->
    </dependency>
</dependencies>
```

3. Shade the dependency into your plugin
```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-shade-plugin</artifactId> <!-- Add this plugin -->
            <version>3.2.4</version>
            <configuration>
                <relocations>
                    <relocation>
                        <pattern>me.partlysunny.commandeer</pattern>
                        <shadedPattern>your.plugin.package.commandeer</shadedPattern> <!-- Add this relocation -->
                    </relocation>
                </relocations>
            </configuration>
        </plugin>
    </plugins>
</build>
```