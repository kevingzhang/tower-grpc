# Try Rust and Node gRPC communication on Towner-grpc

Original readme is [here](./README_origin.md). 
Most of the code are forked from https://github.com/tower-rs/tower-grpc, I added the node.js example from official gRPC.io example. Made a few modification make sure they works together.

The goal of this small project is to demo how to interoperate between Rust and Node using g-RPC using Towner-gRPC

Please only try the route_guide example, because this is the most complete demo for all 4 types of gRPC protocol. 

You can run server and client in both Rust or Node, they are interoperatable.

## For example, run Rust server and node client
In one terminal
``` bash
$ cd tower-grpc-examples
$ RUST_BACKTRACE=1 cargo run --bin route-guide-server ./data/route_guide_db.json
```
In another terminal
```bash
$ cd /node-examples/dynamic_codegen/route_guide
$ node route_guide_client.js 
```
Assume you know how to ```npm install``` to setup the node.

You can also try to run node server and rust client vice versa.

## Try other languages

In official gRPC examples, there are many other languages, all of them should work. Just make sure they share the same proto file and data file.

