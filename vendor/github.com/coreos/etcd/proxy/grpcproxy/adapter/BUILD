load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "chan_stream.go",
        "cluster_client_adapter.go",
        "doc.go",
        "election_client_adapter.go",
        "kv_client_adapter.go",
        "lease_client_adapter.go",
        "lock_client_adapter.go",
        "maintenance_client_adapter.go",
        "watch_client_adapter.go",
    ],
    importpath = "github.com/coreos/etcd/proxy/grpcproxy/adapter",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/coreos/etcd/etcdserver/api/v3election/v3electionpb:go_default_library",
        "//vendor/github.com/coreos/etcd/etcdserver/api/v3lock/v3lockpb:go_default_library",
        "//vendor/github.com/coreos/etcd/etcdserver/etcdserverpb:go_default_library",
        "//vendor/golang.org/x/net/context:go_default_library",
        "//vendor/google.golang.org/grpc:go_default_library",
        "//vendor/google.golang.org/grpc/metadata:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
