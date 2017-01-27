#
# docker image build -t intellij:2016.3.3 .
#
# docker run -it -v /tmp/.X11-unix:/tmp/.X11-unix \
#   -e DISPLAY=${DISPLAY} intellij:2016.3.3
#
FROM openjdk:8-jdk

RUN curl -sSL https://download.jetbrains.com/idea/ideaIC-2016.3.3-no-jdk.tar.gz -o /tmp/ideaIC-2016.3.3-no-jdk.tar.gz \
    && tar -xzvf /tmp/ideaIC-2016.3.3-no-jdk.tar.gz -C /opt \
    && rm -rf /tmp/*.tar.gz

VOLUME ["/root"]

ENTRYPOINT ["/opt/idea-IC-163.11103.6/bin/idea.sh"]
