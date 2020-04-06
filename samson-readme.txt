Readme - samson

mtcnn_facenet_cpp_tensorRT

https://github.com/nwesem/mtcnn_facenet_cpp_tensorRT

https://github.com/samsonadmin/mtcnn_facenet_cpp_tensorRT

modify the CMakeLists.txt


mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make -j${nproc}

-gencode arch=compute_53,code=sm_53


Run from the build direcory
./mtcnn_facenet_cpp_tensorRT

Building the engines before running takes
for 720p res
started from 7.16am
more than 20mins 


To modify the src resolution

[src/main.cpp]
int videoFrameWidth = 1080; //samson
int videoFrameHeight = 720; //samson

VideoStreamer videoStreamer = VideoStreamer(0, videoFrameWidth, videoFrameHeight, 30, isCSICam);

remove the built engine files
rm ../facenetModels/facenet.uff
rm ../facenetModels/facenet.engine
rm ../mtCNNModels/*.engine




