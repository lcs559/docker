# The MIT License
#
#  Copyright (c) 2015-2020, CloudBees, Inc. and other Jenkins contributors
#
#  Permission is hereby granted, free of charge, to any person obtaining a copy
#  of this software and associated documentation files (the "Software"), to deal
#  in the Software without restriction, including without limitation the rights
#  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
#  copies of the Software, and to permit persons to whom the Software is
#  furnished to do so, subject to the following conditions:
#
#  The above copyright notice and this permission notice shall be included in
#  all copies or substantial portions of the Software.
#
#  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
#  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
#  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
#  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
#  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
#  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
#  THE SOFTWARE.

# There is no official Alpine images at the moment.
# Needs upgrade when/if there is an official alpine image.
FROM liaocs559/jenkins-agent:4.7-1-jdk8-centos7-maven.1

ARG root_user=root
ARG jenkins_user=jenkins

ADD node-v12.16.1-linux-x64.tar.gz  /usr/local/

USER ${root_user}

RUN  ln -s /usr/local/node-v12.16.1-linux-x64/bin/npm  /usr/local/bin/ \
    &&  ln -s /usr/local/node-v12.16.1-linux-x64/bin/node /usr/local/bin/ \
    && npm i npm -g \
    && echo "Asia/shanghai" > /etc/timezone

USER ${jenkins_user}

CMD <"npm -v","node -v">