#Download base image centos
FROM centos:latest

WORKDIR /opt/prometheus

# Install prometeus
RUN curl -L 'https://github.com/prometheus/prometheus/releases/download/v2.10.0/prometheus-2.10.0.linux-amd64.tar.gz' -o /tmp/prometheus.tar.gz
RUN tar -xf /tmp/prometheus.tar.gz -C /opt/prometheus/ --strip-components 1

CMD ["/opt/prometheus/prometheus", "--web.enable-lifecycle", "--web.enable-admin-api", "--storage.tsdb.retention.time", "7d"]
EXPOSE 9090
