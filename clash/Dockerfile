FROM ubuntu:20.04

WORKDIR /clash
COPY . /clash

# RUN apt-get update && apt-get upgrade && apt-get install -y \
#   wget

ADD https://github.com/MetaCubeX/Clash.Meta/releases/download/v1.14.0/Clash.Meta-linux-amd64-v1.14.0.gz clash.gz

RUN gzip -d clash.gz

RUN chmod +x clash

CMD ["./clash", "-d", "conf"]

EXPOSE 7890

# CMD ["Clash.Meta-linux-amd64-v1.14.0", "-d", "conf"]

# CMD ["sh", "-c", "tail -f /dev/null"]

# ENTRYPOINT ["~/clash/Clash.Meta-linux-amd64-v1.14.0/Clash.Meta-linux-amd64"]