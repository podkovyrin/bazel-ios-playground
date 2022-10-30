load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

swift_library(
    tags = ["manual"],
    name = "Sources",
    srcs =  glob(["*.swift"]),
    data = [
        "Assets.xcassets",
        "Base.lproj",
    ],
)

ios_application(
    name = "bzl-playground",
    bundle_id = "io.1inchtest.bzl-playground",
    families = [
        "iphone",
        "ipad",
    ],
    minimum_os_version = "15.0",
    infoplists = [":Info.plist"],
    visibility = ["//visibility:public"],
    deps = [":Sources"],
)
