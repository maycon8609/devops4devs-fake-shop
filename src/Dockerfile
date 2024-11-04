FROM python:3.11-slim
COPY requirements.txt .
RUN python -m pip install --no-cache-dir -r requirements.txt
WORKDIR /app
COPY . /app
ENV PROMETHEUS_MULTIPROC_DIR=/tmp/metrics
RUN mkdir -p /tmp/metrics && chmod +x /app/entrypoint.sh
EXPOSE 5000
CMD ["/app/entrypoint.sh"]
