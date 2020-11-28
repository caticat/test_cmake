# cmake版本号限制
cmake_minimum_required(VERSION 2.8.0)

# 项目名
project(t)

# include目录
include_directories(include)

# src目录
aux_source_directory(src SRCS)

# 可执行程序输出目录
set(EXECUTABLE_OUTPUT_PATH bin)

# 生成可执行文件 参数1:可执行文件名 参数2:所有的源代码目录
add_executable(${PROJECT_NAME} ${SRCS})

# 以上内容已经可以生成当前项目的可执行文件了
# 下面是其他常用的内容

# 输出测试日志
# message(STATUS "测试输出:" ${PROJECT_NAME})

# 添加lib库目录(-L)
# link_directories(/usr/lib64)

# 添加lib库(-l) 可以同时添加多个
# add_library(-lprotobuf -lpthread)
# target_link_libraries(${PROJECT_NAME} -lprotobuf -lpthread -ljson_linux-gcc-4.8.5_libmt -lmysqlclient -lpython2.7 -rdynamic -ldl -lz)
