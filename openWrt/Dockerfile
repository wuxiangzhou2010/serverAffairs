FROM ubuntu
RUN \
 apt-get update 
RUN \
 apt-get install -y --no-install-recommends git-core build-essential libssl-dev \
 wget libncurses5-dev unzip gawk zlib1g-dev  subversion mercurial ca-certificates apt-utils file &&\
 apt-get clean
RUN \
 git clone https://github.com/openwrt/openwrt.git
RUN \
 cd openwrt &&\
 ./scripts/feeds update -a &&\
 ./scripts/feeds install -a
RUN apt-get install -y file
