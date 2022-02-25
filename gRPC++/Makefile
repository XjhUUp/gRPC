LDFLAGS = -L/usr/local/lib `pkg-config --libs protobuf grpc++ opencv` \
           -Wl,--no-as-needed -lgrpc++_reflection -Wl,--as-needed\
           -ldl -lpthread

CXX = g++
CPPFLAGS += `pkg-config --cflags protobuf grpc`
CXXFLAGS += -std=c++11

GRPC_CPP_PLUGIN = grpc_cpp_plugin
GRPC_CPP_PLUGIN_PATH ?= `which $(GRPC_CPP_PLUGIN)`

all: client server

client: demo.pb.o demo.grpc.pb.o client.o
	$(CXX) $^ $(LDFLAGS) -o $@

server: demo.pb.o demo.grpc.pb.o server.o
	$(CXX) $^ $(LDFLAGS) -o $@

%.grpc.pb.cc: %.proto
	protoc --grpc_out=. --plugin=protoc-gen-grpc=$(GRPC_CPP_PLUGIN_PATH) $<

%.pb.cc: %.proto
	protoc --cpp_out=. $<

clean:
	rm -f *.o *.pb.cc *.pb.h client server

	185.199.108.133	raw.githubusercontent.com
185.199.109.133	raw.githubusercontent.com
185.199.110.133	raw.githubusercontent.com
185.199.111.133	raw.githubusercontent.com
140.82.113.4	github.com
199.232.69.194	github.global.ssl.fastly.net
185.199.108.153 assets-cdn.github.com
185.199.109.153 assets-cdn.github.com
185.199.110.153 assets-cdn.github.com
185.199.111.153 assets-cdn.github.com


fatal: unable to access 'https://github.com/xjh19971110/gRPC/git/': gnutls_handshake() failed: The TLS connection was non-properly terminated.
