set(SRCS
    Channel.cpp
    Epoll.cpp
    EventLoop.cpp
    EventLoopThread.cpp
    EventLoopThreadPool.cpp
    HttpData.cpp
    Main.cpp
    Server.cpp
    #ThreadPool.cpp
    Timer.cpp
    Util.cpp
)
include_directories(${PROJECT_SOURCE_DIR}/base)


add_executable(zexweb ${SRCS})
target_link_libraries(zexweb libserver_base)


add_subdirectory(base)
add_subdirectory(tests)