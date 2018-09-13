# SPRING CHEAT SHEET FOR LINUX
> Spring framework start guide for Linux

## Required JAVA

### Install JAVA

```sh
# install java oracle 8
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer

# set default java
sudo apt-get install oracle-java8-set-default
```

### SET JAVA_HOME
> set env JAVA_HOME to your shell profile (~/.zshrc)
```sh
export JAVA_HOME=/usr/lib/jvm/java-8-oracle
```

## Install Spring Boot via SDKMan

```sh
# install maven
sudo apt install maven

# install sdkman (https://sdkman.io/install) for spring-cli 
curl -s "https://get.sdkman.io" | bash
source "$HOME/.sdkman/bin/sdkman-init.sh"

# install springboot cli via sdkman
sdk install springboot
```

# Init project via spring-cli
> Docs [https://docs.spring.io/spring-boot/docs/2.0.5.RELEASE/reference/htmlsingle/#cli-init](https://docs.spring.io/spring-boot/docs/2.0.5.RELEASE/reference/htmlsingle/#cli-init)

```sh
spring init --dependencies=ws my-project
```

# Run Project with maven

```sh
mvn spring-boot:run # default port 8080 for web service

# or for run with maven local project
./mvnw spring-boot:run
```