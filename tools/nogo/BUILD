load("//tools:defs.bzl", "bzl_library", "go_library")
load("//tools/nogo:defs.bzl", "nogo_dump_tool", "nogo_stdlib")

package(licenses = ["notice"])

nogo_dump_tool(
    name = "dump_tool",
    visibility = ["//visibility:public"],
)

nogo_stdlib(
    name = "stdlib",
    visibility = ["//visibility:public"],
)

go_library(
    name = "nogo",
    srcs = [
        "build.go",
        "config.go",
        "matchers.go",
        "nogo.go",
        "register.go",
    ],
    nogo = False,
    visibility = ["//:sandbox"],
    deps = [
        "//tools/checkescape",
        "//tools/checkunsafe",
        "@org_golang_x_tools//go/analysis:go_tool_library",
        "@org_golang_x_tools//go/analysis/internal/facts:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/asmdecl:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/assign:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/atomic:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/bools:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/buildtag:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/cgocall:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/composite:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/copylock:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/errorsas:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/httpresponse:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/loopclosure:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/lostcancel:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/nilfunc:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/nilness:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/printf:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/shadow:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/shift:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/stdmethods:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/stringintconv:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/structtag:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/tests:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/unmarshal:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/unreachable:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/unsafeptr:go_tool_library",
        "@org_golang_x_tools//go/analysis/passes/unusedresult:go_tool_library",
        "@org_golang_x_tools//go/gcexportdata:go_tool_library",
    ],
)

bzl_library(
    name = "defs_bzl",
    srcs = ["defs.bzl"],
    visibility = ["//visibility:private"],
)
