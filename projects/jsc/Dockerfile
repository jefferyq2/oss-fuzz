# Copyright 2017 Google Inc.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
################################################################################

FROM gcr.io/oss-fuzz-base/base-builder
MAINTAINER ochang@google.com
RUN apt-get update && apt-get install -y cmake make autoconf automake libtool python ruby ninja-build bison flex gperf wget
RUN git clone --depth 1 git://git.webkit.org/WebKit.git
RUN wget http://download.icu-project.org/files/icu4c/60.1/icu4c-60_1-src.tgz && tar xzvf icu4c-60_1-src.tgz
WORKDIR WebKit
COPY build.sh $SRC