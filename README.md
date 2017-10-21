# rookery

[![Concourse](https://wings.concourse.ci/api/v1/teams/code-bandits/pipelines/rookery/jobs/publish/badge)](https://wings.concourse.ci/teams/code-bandits/pipelines/rookery)

Rookery is an evolving Concourse task container image. It supplies functionality to the build including:

- Google Chrome, ChromeDriver, and Xvfb for use in browser tests
- OpenJDK JDK 8
- MySQL Server

## Usage

In your Concourse task definitions:

```yaml
# Use a specific version

platform: linux
image_resource:
  type: docker-image
  source: {repository: codebandits/rookery, tag: 0.0.1}
run: ...
```

```yaml
# Use the latest version

platform: linux
image_resource:
  type: docker-image
  source: {repository: codebandits/rookery}
run: ...
```

The available tags are listed here: https://hub.docker.com/r/codebandits/rookery/tags/
