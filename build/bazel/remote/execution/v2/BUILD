package(default_visibility = ["//visibility:public"])
load("@com_github_grpc_grpc//bazel:cc_grpc_library.bzl", "cc_grpc_library")

licenses(["notice"])

proto_library(
    name = "remote_execution_proto",
    srcs = ["remote_execution.proto"],
    deps = [
        "//build/bazel/semver:semver_proto",
        "@com_google_protobuf//:duration_proto",
        "@com_google_protobuf//:timestamp_proto",
        "@googleapis//:google_api_annotations_proto",
        "@googleapis//:google_api_http_proto",
        "@googleapis//:google_longrunning_operations_proto",
        "@googleapis//:google_rpc_status_proto",
    ],
)

java_proto_library(
    name = "remote_execution_java_proto",
    deps = [":remote_execution_proto"],
)

cc_grpc_library(
    name = "remote_execution_cc_proto",
    srcs = ["remote_execution.proto"],
    deps = [
        "//build/bazel/semver:semver_cc_proto",
        "@googleapis//:google_api_annotations_cc_proto",
        "@googleapis//:google_api_http_cc_proto",
        "@googleapis//:google_longrunning_operations_cc_proto",
        "@googleapis//:google_rpc_status_cc_proto",
    ],
    proto_only = False,
    well_known_protos = True,
    use_external = False,
)

