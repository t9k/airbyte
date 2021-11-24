# T9k Fork of Airbyte

## 编译镜像

根据 [Airbyte 开发者文档](./docs/contributing-to-airbyte/developing-locally.md)，下载 [OpenJDK 14.0.2](https://jdk.java.net/archive/) 并解压。

使用如下命令编译镜像：

```bash
export JAVA_HOME=/path/to/jdk-14.0.2.jdk/Contents/Home
export VERSION=0.32.5-alpha
./gradlew :airbyte-webapp:assemble

# wait for building...

docker tag airbyte/webapp:${VERSION} tsz.io/t9k/airbyte-webapp:${VERSION}
docker push tsz.io/t9k/airbyte-webapp:${VERSION}
```

## 部署

见 https://github.com/t9k/apps/blob/master/airbyte/README.md
