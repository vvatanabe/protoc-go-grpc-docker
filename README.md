# protoc-go-grpc-docker
Protocol Buffers compilation for Go and gRPC

## Install

```sh
$ docker pull ghcr.io/vvatanabe/protoc-go-grpc-docker/protoc-go-grpc:v0.0.1
```

## Usage

```sh
$ docker run -it --rm \
  -v $(pwd):/protoc-go-grpc \
  ghcr.io/vvatanabe/protoc-go-grpc-docker/protoc-go-grpc:v0.0.1 [OPTION] PROTO_FILES
```

## Example

```sh
$ docker run -it --rm \
  -v $(pwd):/protoc-go-grpc \
  ghcr.io/vvatanabe/protoc-go-grpc-docker/protoc-go-grpc:v0.0.1 \
    --go_out=. --go_opt=paths=source_relative \
    --go-grpc_out=. --go-grpc_opt=paths=source_relative \
    helloworld/helloworld.proto
```

## License

[MIT License](http://www.opensource.org/licenses/mit-license.php)

## Author

[vvatanabe](https://github.com/vvatanabe)
