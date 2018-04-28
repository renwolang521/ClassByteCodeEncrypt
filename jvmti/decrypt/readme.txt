cd decrypt

g++ -fPIC  -I /usr/java/default/include -I /usr/java/default/include/linux -c decrypt.cpp  

g++ -fPIC  -shared  -o liblinux.so decrypt.o

export LD_LIBRARY_PATH=${LD_LIBRARY_PATH}:~/decrypt

java -agentlib:linux  test.MyTest