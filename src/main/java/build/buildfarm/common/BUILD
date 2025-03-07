java_library(
    name = "common",
    srcs = glob([
        "*.java",
        "function/*.java",
        "io/*.java",
        "redis/*.java",
    ]),
    plugins = [":lombok"],
    visibility = ["//visibility:public"],
    deps = [
        "//src/main/java/build/buildfarm/common/resources",
        "//src/main/java/build/buildfarm/common/resources:resource_java_proto",
        "//src/main/protobuf:build_buildfarm_v1test_buildfarm_java_proto",
        "//third_party/jedis",
        "@googleapis//:google_longrunning_operations_java_proto",
        "@googleapis//:google_rpc_code_java_proto",
        "@googleapis//:google_rpc_error_details_java_proto",
        "@maven//:com_github_jnr_jnr_constants",
        "@maven//:com_github_jnr_jnr_ffi",
        "@maven//:com_github_jnr_jnr_posix",
        "@maven//:com_github_luben_zstd_jni",
        "@maven//:com_google_code_findbugs_jsr305",
        "@maven//:com_google_guava_failureaccess",
        "@maven//:com_google_guava_guava",
        "@maven//:com_google_protobuf_protobuf_java",
        "@maven//:com_google_protobuf_protobuf_java_util",
        "@maven//:commons_io_commons_io",
        "@maven//:io_grpc_grpc_api",
        "@maven//:io_grpc_grpc_context",
        "@maven//:io_grpc_grpc_protobuf",
        "@maven//:io_prometheus_simpleclient",
        "@maven//:org_apache_commons_commons_compress",
        "@maven//:org_projectlombok_lombok",
        "@maven//:org_threeten_threetenbp",
        "@remote_apis//:build_bazel_remote_execution_v2_remote_execution_java_proto",
    ],
)

java_plugin(
    name = "lombok",
    generates_api = True,
    processor_class = "lombok.launch.AnnotationProcessorHider$AnnotationProcessor",
    visibility = ["//visibility:public"],
    deps = ["@maven//:org_projectlombok_lombok"],
)
