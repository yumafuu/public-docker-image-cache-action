# public-docker-image-cache-action

Cache public docker image ( like `mysql:8.0`, `redis:7.2` ) using GitHub Actions cache([actions/cache](https://github.com/actions/cache)).

This is created for stable image like `mysql:8.0`, `redis:7.2` which is not changed frequently for your project.

How many times do you pull `mysql:8.0` image from docker hub in your CI/CD pipeline?

It is very MOTTAINAI!

## Usage

```yaml
name: Sample Workflow

jobs:
    build:
        name: Cache mysql:8.0
        runs-on: ubuntu-latest
        steps:
            - uses: YumaFuu/public-docker-image-cache-action@v1
              with:
                image: mysql:8.0
```

## Thanks

This action is inspired by below question. <br>
[How to run cached Docker image in Github Action? - Stack Overflow](https://stackoverflow.com/questions/66421411/how-to-run-cached-docker-image-in-github-action)
