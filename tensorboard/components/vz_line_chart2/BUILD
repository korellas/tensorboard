package(default_visibility = ["//tensorboard:internal"])

load("//tensorboard/defs:defs.bzl", "tensorboard_webcomponent_library")
load("//tensorboard/defs:web.bzl", "tf_web_library")

licenses(["notice"])  # Apache 2.0

tf_web_library(
    name = "vz_line_chart2",
    srcs = [
        "line-chart-exporter.ts",
        "line-chart.ts",        
        "linear-scale.ts",
        "log-scale.ts",
        "panZoomDragLayer.html",
        "panZoomDragLayer.ts",
        "tf-scale.ts",
        "vz-line-chart2.html",
        "vz-line-chart2.ts",
    ],
    path = "/vz-line-chart2",
    visibility = ["//visibility:public"],
    deps = [
        "//tensorboard/components/tf_imports:d3",
        "//tensorboard/components/tf_imports:lodash",
        "//tensorboard/components/tf_imports:plottable",
        "//tensorboard/components/tf_imports:polymer",
        "//tensorboard/components/vz_chart_helpers",
        "//tensorboard/components/vz_line_chart:dragZoomInteraction",
    ],
)

tensorboard_webcomponent_library(
    name = "legacy",
    srcs = [":vz_line_chart2"],
    destdir = "vz-line-chart2",
    deps = [
        "//tensorboard/components/tf_imports:polymer_lib",
        "//tensorboard/components/tf_imports_google:lib",
        "//tensorboard/components/vz_chart_helpers:legacy",
        "//tensorboard/components/vz_line_chart:dragZoomInteraction_legacy",
    ],
)
