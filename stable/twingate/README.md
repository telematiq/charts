# Twingate Connector

```
$ helm repo add twingate https://twingate.github.io/helm-charts
$ helm upgrade --install my-release twingate/connector -n [namespace] \
    --set connector.network=[network] \
    --set connector.accessToken=[accessToken] \
    --set connector.refreshToken=[refreshToken]
```

Using secret for access/refresh token

```
apiVersion: v1
kind: Secret
metadata:
  name: my-secret
type: Opaque
data:
  TWINGATE_ACCESS_TOKEN: "your access token base64 encoded"
  TWINGATE_REFRESH_TOKEN: "your refresh token base64 encoded"
```

