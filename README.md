# envsubst 

解决最新版glibc 2.29库依赖问题

## envsubst alpine docker images


简单使用方法
~~~sh
docker run -e APP_NAME="My Alpine Envsubst Test app" tekintian/alpine-envsubst /tmp/test.txt
~~~

更多详情 https://hub.docker.com/r/tekintian/alpine-envsubst


## envsubst 命令详解

用shell格式字符串中的值替换环境变量。要替换的变量应位于${var}或$var格式。

替换环境变量stdin输出到stdout:

echo '{{$HOME}}' | envsubst

将输入文件中的环境变量替换为stdout:

envsubst < {{path/to/input_file}}

将输入文件中的环境变量替换为文件，并将其输出到文件中：

envsubst < {{path/to/input_file}} > {{path/to/output_file}}


用空格分隔的列表，替换输入文件中的环境变量：

envsubst '{{$USER $SHELL $HOME}}' < {{path/to/input_file}}



