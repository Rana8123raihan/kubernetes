package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["storage_test.go"],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/errors:go_default_library",
        "//pkg/api/errors/storage:go_default_library",
        "//pkg/api/rest:go_default_library",
        "//pkg/fields:go_default_library",
        "//pkg/genericapiserver/api/request:go_default_library",
        "//pkg/registry/generic:go_default_library",
        "//pkg/registry/registrytest:go_default_library",
        "//pkg/securitycontext:go_default_library",
        "//pkg/storage:go_default_library",
        "//pkg/storage/etcd/testing:go_default_library",
        "//vendor:golang.org/x/net/context",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/labels",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/util/diff",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "eviction.go",
        "storage.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/errors:go_default_library",
        "//pkg/api/errors/storage:go_default_library",
        "//pkg/api/rest:go_default_library",
        "//pkg/api/validation:go_default_library",
        "//pkg/apis/policy:go_default_library",
        "//pkg/client/clientset_generated/internalclientset/typed/policy/internalversion:go_default_library",
        "//pkg/client/retry:go_default_library",
        "//pkg/genericapiserver/api/request:go_default_library",
        "//pkg/kubelet/client:go_default_library",
        "//pkg/registry/core/pod:go_default_library",
        "//pkg/registry/core/pod/rest:go_default_library",
        "//pkg/registry/generic:go_default_library",
        "//pkg/registry/generic/registry:go_default_library",
        "//pkg/storage:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/labels",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/util/wait",
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
)