package(default_visibility = ["//tensorflow:internal"])

load("@io_bazel_rules_closure//closure:defs.bzl", "web_library")

licenses(["notice"])  # Apache 2.0

web_library(
    name = "vz_histogram_timeseries_d3v4",
    srcs = ["vz-histogram-timeseries.html"],
    path = "/vz-histogram-timeseries",
    deps = [
        "//tensorflow/tensorboard/components/tf_imports_d3v4:d3",
        "@org_polymer",
    ],
)

web_library(
    name = "demo",
    srcs = ["index.html"],
    path = "/vz-histogram-timeseries",
    deps = [
        ":vz_histogram_timeseries_d3v4",
        "@org_polymer_iron_demo_helpers",
        "@org_polymer_paper_button",
        "@org_polymer_paper_styles",
        "@org_polymer_webcomponentsjs",
    ],
)

filegroup(
    name = "all_files",
    srcs = glob(["**"]),
    tags = ["notsan"],
)
