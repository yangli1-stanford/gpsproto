The gps_trajectory.proto Format
-------------------------------------------------------

### Dependency ###

Google Protocol Buffers

  <https://developers.google.com/protocol-buffers>


### Compile protobuf class ###

   Go to `proto/`, compile the format file `gps_trajectory.proto`

    protoc -I=. --cpp_out=. gps_trajectory.proto

   This will generate `proto/gps_trajectory.pb.h` and
   
   `proto/gps_trajectory.pb.cc`


### Compile & Run Example ###

Create a build directory

    mkdir build;
    cd build;

Call cmake and make

    cmake ..;
    make;

Inside `build/`, call gpsproto on a test trajectory file:

    ./gpsproto ../test.pbf test_out.pbf

test.pbf and test_out.pbf should be the same.


