# sto-core

![Version: 0.2.4](https://img.shields.io/badge/Version-0.2.4-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.0.1](https://img.shields.io/badge/AppVersion-0.0.1-informational?style=flat-square)

A Helm chart for Kubernetes

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | common | 2.x.x |
| https://harness.github.io/helm-common | harness-common | 1.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `true` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| env.config.APP_ENABLE_UI | bool | `true` |  |
| env.config.APP_HARNESS_TOKEN | string | `"test"` |  |
| env.config.APP_INTERNAL_TOKEN_JWT_SECRET | string | `"test"` |  |
| env.config.APP_TOKEN_JWT_SECRET | string | `"test"` |  |
| env.secrets | string | `nil` |  |
| fullnameOverride | string | `""` |  |
| global.loadbalancerURL | string | `"http://test/"` |  |
| image.digest | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"harness/stocore-signed"` |  |
| image.tag | string | `"v2-alpha15"` |  |
| ingress.annotations."kubernetes.io/ingress.class" | string | `"nginx"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/rewrite-target" | string | `"/api/v2"` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].paths[0].path | string | `"/sto/api/v2"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| maxSurge | string | `"100%"` |  |
| maxUnavailable | int | `0` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| postgresPassword.key | string | `"postgres-password"` |  |
| postgresPassword.name | string | `"postgres"` |  |
| replicaCount | int | `1` |  |
| resources.requests.cpu | string | `"500m"` |  |
| resources.requests.memory | string | `"500Mi"` |  |
| securityContext | object | `{}` |  |
| service.port | int | `4000` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `"harness-default"` |  |
| stoAppAuditJWTSecret.key | string | `"stoAppAuditJWTSecret"` |  |
| stoAppAuditJWTSecret.name | string | `"harness-secrets"` |  |
| stoAppHarnessToken.key | string | `"stoAppHarnessToken"` |  |
| stoAppHarnessToken.name | string | `"harness-secrets"` |  |
| tolerations | list | `[]` |  |
| waitForInitContainer.image.digest | string | `""` |  |
| waitForInitContainer.image.pullPolicy | string | `"IfNotPresent"` |  |
| waitForInitContainer.image.registry | string | `"docker.io"` |  |
| waitForInitContainer.image.repository | string | `"harness/helm-init-container"` |  |
| waitForInitContainer.image.tag | string | `"latest"` |  |

