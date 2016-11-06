CMAKE_MINIMUM_REQUIRED ( VERSION 2.8 )

PROJECT ( SnowSim )

FIND_PACKAGE ( OpenGL REQUIRED )
FIND_PACKAGE ( GLFW3 REQUIRED )
FIND_PACKAGE ( Threads REQUIRED )

ADD_EXECUTABLE ( snowsim
  Grid.cpp
  Matrix2f.cpp
  Particle.cpp
  PointCloud.cpp
  Shape.cpp
  Vector2f.cpp
  main.cpp
  )

TARGET_LINK_LIBRARIES ( snowsim
  ${GLFW3_LIBRARIES}
  ${CMAKE_THREAD_LIBS_INIT}
  )
