# tracing-demo
A demo application, based on [Jaeger Hot R.O.D](https://github.com/jaegertracing/jaeger/tree/master/examples/hotrod), to submit example traces to [Logz.io's distributed tracing product](https://logz.io/platform/distributed-tracing/).

This demo application is used by Logz.io's guide to ["Sending demo traces with the HotROD application"](https://docs.logz.io/user-guide/distributed-tracing/trace-hotrod-demo).

## Prerequisites
- [Docker](https://docs.docker.com/get-docker/)

## Getting Started
Update the `.env` file in this repo with your [tracing account token](https://docs.logz.io/user-guide/distributed-tracing/getting-started-tracing/) and [region code](https://docs.logz.io/user-guide/accounts/account-region.html#available-regions).

For example:
```
ACCOUNT_TOKEN=MyAccountToken
REGION_CODE=us
```

Create External network
```
docker network create dockercompose_testcluster
```

Start the demo:
```
docker-compose up
```

Open http://127.0.0.1:18080 and click on the buttons to send traces.

`Ctrl+C` to stop the demo and then remove the containers with:
```
docker-compose down
```

## Additional References
- [Logz.io Distributed Tracing - User Guide](https://docs.logz.io/user-guide/distributed-tracing/)
- [Logz.io Distributed Tracing - Getting Started](https://docs.logz.io/user-guide/distributed-tracing/getting-started-tracing/)
