load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "collector.go",
        "collector-http.go",
        "collector-kafka.go",
        "collector-scribe.go",
        "context.go",
        "debug.go",
        "event.go",
        "log-materializers.go",
        "logger.go",
        "propagation.go",
        "propagation_ot.go",
        "raw.go",
        "recorder.go",
        "sample.go",
        "span.go",
        "tracer.go",
        "util.go",
        "zipkin-endpoint.go",
        "zipkin-recorder.go",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/Shopify/sarama:go_default_library",
        "//vendor/github.com/apache/thrift/lib/go/thrift:go_default_library",
        "//vendor/github.com/go-logfmt/logfmt:go_default_library",
        "//vendor/github.com/gogo/protobuf/proto:go_default_library",
        "//vendor/github.com/opentracing/opentracing-go:go_default_library",
        "//vendor/github.com/opentracing/opentracing-go/ext:go_default_library",
        "//vendor/github.com/opentracing/opentracing-go/log:go_default_library",
        "//vendor/github.com/openzipkin/zipkin-go-opentracing/_thrift/gen-go/scribe:go_default_library",
        "//vendor/github.com/openzipkin/zipkin-go-opentracing/_thrift/gen-go/zipkincore:go_default_library",
        "//vendor/github.com/openzipkin/zipkin-go-opentracing/flag:go_default_library",
        "//vendor/github.com/openzipkin/zipkin-go-opentracing/types:go_default_library",
        "//vendor/github.com/openzipkin/zipkin-go-opentracing/wire:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "bench_test.go",
        "collector-http_test.go",
        "collector-kafka_test.go",
        "collector-scribe_test.go",
        "collector_test.go",
        "concurrency_test.go",
        "log-materializers_test.go",
        "recorder_test.go",
        "span_test.go",
        "testutil_test.go",
    ],
    library = ":go_default_library",
    deps = [
        "//vendor/github.com/Shopify/sarama:go_default_library",
        "//vendor/github.com/apache/thrift/lib/go/thrift:go_default_library",
        "//vendor/github.com/opentracing/opentracing-go:go_default_library",
        "//vendor/github.com/opentracing/opentracing-go/ext:go_default_library",
        "//vendor/github.com/opentracing/opentracing-go/log:go_default_library",
        "//vendor/github.com/openzipkin/zipkin-go-opentracing/_thrift/gen-go/scribe:go_default_library",
        "//vendor/github.com/openzipkin/zipkin-go-opentracing/_thrift/gen-go/zipkincore:go_default_library",
        "//vendor/github.com/stretchr/testify/assert:go_default_library",
    ],
)

go_test(
    name = "go_default_xtest",
    srcs = [
        "propagation_test.go",
        "sample_test.go",
    ],
    deps = [
        "//vendor/github.com/davecgh/go-spew/spew:go_default_library",
        "//vendor/github.com/opentracing/opentracing-go:go_default_library",
        "//vendor/github.com/openzipkin/zipkin-go-opentracing:go_default_library",
        "//vendor/github.com/openzipkin/zipkin-go-opentracing/flag:go_default_library",
        "//vendor/github.com/openzipkin/zipkin-go-opentracing/types:go_default_library",
    ],
)
