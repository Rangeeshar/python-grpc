# python-grpc
A simple python grpc client and server implementation

- Create a virtual env with requirements.txt file


For implementing gRPC services, we need to define three files:-

Proto file - Proto file comprises the declaration of the service that is used to generate stubs (<package_name>_pb2.py and <package_name>_pb2_grpc.py). These are used by the gRPC client and the gRPC server.</package_name></package_name>
gRPC client - The client makes a gRPC call to the server to get the response as per the proto file.‍
gRPC Server - The server is responsible for serving requests to the client.

proto file explanation:

we have declared a service named Unary. It consists of a collection of services. For now, I have implemented a single service GetServerResponse(). This service takes an input of type Message and returns a MessageResponse. Below the service declaration, I have declared Message and Message Response.

- python -m grpc_tools.protoc --proto_path=. ./unary.proto --python_out=. --grpc_python_out=.
- python3 unary_server.py
- python3 unary_client.py