load("@score_tooling//coverage:defs.bzl", "score_coverage_reporter", "score_coverage_scope")

score_coverage_scope(
    name = "coverage_scope",
    testonly = True,
    deps = [
        # "//score/mw/log:frontend",
        # "//score/language/rust/memres:memres"
    ],
)

score_coverage_reporter(
    name = "reporter_wrapper",
    testonly = True,
    coverage_scope = ":coverage_scope",
    llvm_cov = "@llvm_toolchain//:llvm-cov",
    llvm_profdata = "@llvm_toolchain//:llvm-profdata",
    llvm_cxxfilt = "@llvm_toolchain_llvm//:bin/llvm-cxxfilt",
)