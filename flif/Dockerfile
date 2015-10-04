FROM debian:latest
MAINTAINER Jordan Krage "jmank88@gmail.com"

# Install git
RUN apt-get update && apt-get install -y --no-install-recommends \
    git-core \
    make \
    pkg-config \
    g++ \
    ca-certificates \
    zlib1g-dev \
    libpng-dev \
    && rm -rf /var/lib/apt/lists/*

# Clone https://github.com/jonsneyers/FLIF
RUN git clone https://github.com/jonsneyers/FLIF /FLIF

#Build
RUN cd /FLIF && \
    make

CMD ["/FLIF/flif"]
