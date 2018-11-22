## Introduction

This chart bootstraps a single node PostgreSQL deployment on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Configuration

The following table lists the configurable parameters of the MariaDB chart and their default values.

|             Parameter                     |                     Description                     |                              Default                              |
|-------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------|
| `image.name`                              | PostgreSQL image name                               | `postgres`                                                        |
| `image.tag`                               | PostgreSQL Image tag                                | `11.1-alpine`                                                     |
| `image.pullPolicy`                        | PostgreSQL image pull policy                        | `IfNotPresent`                                                    |
| `db.user`                                 | Username of new user to create                      | `nil`                                                             |
| `db.password`                             | Password for the new user                           | `nil`                                                             |
| `db.name`                                 | Name for new database to create                     | `nil`                                                             |
| `affinity`                                | Affinity                                            | `{}`                                                              |
| `tolerations`                             | List of node taints to tolerate (master)            | `[]`                                                              |
| `storage.class`                           | Persistent Volume Storage Class                     | ``                                                                |
| `storage.size`                            | Persistent Volume Size                              | `8Gi`                                                             |
| `livenessProbe.initialDelaySeconds`       | Delay before liveness probe is initiated            | `30`                                                             |
| `livenessProbe.periodSeconds`             | How often to perform the probe                      | `10`                                                              |
| `livenessProbe.timeoutSeconds`            | When the probe times out                            | `1`                                                               |
| `livenessProbe.successThreshold`          | Minimum consecutive successes for the probe         | `1`                                                               |
| `livenessProbe.failureThreshold`          | Minimum consecutive failures for the probe          | `3`                                                               |
| `readinessProbe.initialDelaySeconds`      | Delay before readiness probe is initiated           | `30`                                                              |
| `readinessProbe.periodSeconds`            | How often to perform the probe                      | `10`                                                              |
| `readinessProbe.timeoutSeconds`           | When the probe times out                            | `1`                                                               |
| `readinessProbe.successThreshold`         | Minimum consecutive successes for the probe         | `1`                                                               |
| `readinessProbe.failureThreshold`         | Minimum consecutive failures for the probe          | `3`                                                               |
| `resources`                               | resource requests/limit                             | `nil`                                                             |

