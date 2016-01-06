FROM bpye/steamcmd:latest
MAINTAINER Ben Pye <ben@curlybracket.co.uk>

# Install Garry's Mod to /opt/garrysmod/
RUN /opt/steamcmd/steamcmd.sh +login anonymous +force_install_dir /opt/garrysmod \
    +app_update 4020 validate +quit

VOLUME ["/opt/garrysmod/garrysmod/addons", \
        "/opt/garrysmod/garrysmod/cfg", \
        "/opt/garrysmod/garrysmod/data"]

EXPOSE 27015/udp 27015/tcp

ENV LD_LIBRARY_PATH=/opt/garrysmod/bin
ENTRYPOINT ["/opt/garrysmod/srcds_linux"]
