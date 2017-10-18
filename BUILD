# Copyright 2017 The Snappy Authors. All rights reserved.
# Use of this source code is governed by a BSD-style license that can be
# found in the COPYING file. See the AUTHORS file for names of contributors.

licenses(["notice"])  # 3-clause BSD

cc_library(
    name = "snappy",
    srcs = [
        "snappy.cc",
        "snappy-internal.h",
        "snappy-sinksource.cc",
    ],
    hdrs = [
        "snappy.h",
        "snappy-sinksource.h",
    ],
    visibility = ["//visibility:public"],
)

cc_library(
    name = "snappy-c",
    srcs = [
        "snappy-c.cc",
    ],
    hdrs = [
        "snappy-c.h",
    ],
    visibility = ["//visibility:public"],
    deps = [
        ":snappy",
    ],
)

filegroup(
    name = "testdata",
    srcs = glob(["testdata/*"]),
    visibility = ["//visibility:public"],
)

cc_test(
    name = "snappy_unittest",
    size = "large",
    srcs = [
      "snappy-test.cc",
      "snappy_unittest.cc",
    ],
    data = [
        ":testdata",
    ],
    deps = [
        ":snappy",
    ],
)
