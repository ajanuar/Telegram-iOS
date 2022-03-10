load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive", "http_file")

http_archive(
    name = "com_google_protobuf",
    urls = ["https://github.com/protocolbuffers/protobuf/archive/v3.14.0.zip"],
    sha256 = "bf0e5070b4b99240183b29df78155eee335885e53a8af8683964579c214ad301",
    strip_prefix = "protobuf-3.14.0",
    type = "zip",
)

load("@com_google_protobuf//:protobuf_deps.bzl", "protobuf_deps")
protobuf_deps()

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")


http_archive(
    name = "build_bazel_rules_apple",
    sha256 = "c84962b64d9ae4472adfb01ec2cf1aa73cb2ee8308242add55fa7cc38602d882",
    url = "https://github.com/bazelbuild/rules_apple/releases/download/0.31.2/rules_apple.0.31.2.tar.gz",
)

load(
    "@build_bazel_rules_apple//apple:repositories.bzl",
    "apple_rules_dependencies",
)

apple_rules_dependencies()

load(
    "@build_bazel_rules_swift//swift:repositories.bzl",
    "swift_rules_dependencies",
)

swift_rules_dependencies()

load(
    "@build_bazel_apple_support//lib:repositories.bzl",
    "apple_support_dependencies",
)

apple_support_dependencies()

load("@bazel_skylib//:workspace.bzl", "bazel_skylib_workspace")

bazel_skylib_workspace()

http_file(
    name = "cmake_tar_gz",
    urls = ["https://github.com/Kitware/CMake/releases/download/v3.19.2/cmake-3.19.2-macos-universal.tar.gz"],
    sha256 = "50afa2cb66bea6a0314ef28034f3ff1647325e30cf5940f97906a56fd9640bd8",
)

http_archive(
    name = "appcenter_sdk",
    urls = ["https://github.com/microsoft/appcenter-sdk-apple/releases/download/4.1.1/AppCenter-SDK-Apple-4.1.1.zip"],
    sha256 = "032907801dc7784744a1ca8fd40d3eecc34a2e27a93a4b3993f617cca204a9f3",
    build_file = "@//third-party/AppCenter:AppCenter.BUILD",
)
