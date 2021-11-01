#1 文档
# 什么是buf [是个什么，能干什么](https://docs.buf.build/introduction)
# grpc-go [grpc-go怎么用](https://grpc.io/docs/languages/go/quickstart/)
# grpc-gateway [grpc-gateway怎么用](https://github.com/grpc-ecosystem/grpc-gateway)

#2 准备工作  
#2.1 安装buf [文档](https://docs.buf.build/installation)  
#2.2 安装go sdk[golang sdk](https://golang.org/dl/)  
#2.3 安装protoc;其实可以不用，有些插件要；所以我们还是装一下[下载地址][https://github.com/protocolbuffers/protobuf/releases]，解压之后移动protoc文件到你的bin目录下，[例如/usr/local/bin, 或者$GOPATH/bin下面] 吧include文件夹下的所有内容放到/usr/local/include下【这一步也可以省略，使用buf管理依赖即可】  
#2.4 安装grpc-go grpc-gateway插件 go install \
    github.com/grpc-ecosystem/grpc-gateway/v2/protoc-gen-grpc-gateway \
    github.com/grpc-ecosystem/grpc-gateway/v2/protoc-gen-openapiv2 \
    google.golang.org/protobuf/cmd/protoc-gen-go \
    google.golang.org/grpc/cmd/protoc-gen-go-grpc  


#2.5 我们使用buf来帮我们生成go代码从而替换protoc 的方式，原因。。。。  protoc命令需要指定插件，指定输入输出目录，有一点繁琐. 
