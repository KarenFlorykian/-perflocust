# perflocust
Docker image with the most recent locust and installed plugins

Example:

1. How to build a Docker image
```bash
$ docker build -t perflocust:latest .
```

2. How to run a test using Docker container
```bash
$ docker run --rm --name=locusttest -v $(pwd):/mnt/locust -w /mnt/locust perflocust:latest -f locustfile.py  -u 1 -r 1 --headless --run-time=30s --print-stats --csv=dockerperf_report --logfile=dockerperf_report.log --html=dockerperf_report.html --log-transactions-in-file --csv-full-history
```