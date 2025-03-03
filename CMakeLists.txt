cmake_minimum_required(VERSION 3.5.0)
project(learngl VERSION 0.1.0 LANGUAGES C CXX)

#add_executable(learngl src/main.cpp ${CMAKE_SOURCE_DIR}/include/glad.c)

add_executable(learngl src/gamer.cpp src/game.cpp src/shader.cpp src/texture.cpp src/resource_manager.cpp src/sprite_renderer.cpp src/game_level.cpp src/game_object.cpp src/ball_object_collisions.cpp src/partical_generator.cpp src/post_processor.cpp ${CMAKE_SOURCE_DIR}/include/glad.c)


link_libraries(learngl lib)

target_link_libraries(learngl PRIVATE ${CMAKE_SOURCE_DIR}/lib/glfw3.lib ${CMAKE_SOURCE_DIR}/lib/irrKlang.lib ${CMAKE_SOURCE_DIR}/lib/assimp-vc143-mtd.lib  ${CMAKE_SOURCE_DIR}/lib/soil2.lib  opengl32 gdi32)



include_directories(learngl include)