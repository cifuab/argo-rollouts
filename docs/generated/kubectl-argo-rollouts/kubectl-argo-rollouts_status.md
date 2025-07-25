# Rollouts Status

Show the status of a rollout

## Synopsis

Watch rollout until it finishes or the timeout is exceeded. Returns success if
the rollout is healthy upon completion and an error otherwise.

```shell
kubectl argo rollouts status ROLLOUT_NAME [flags]
```

## Examples

```shell
# Watch the rollout until it succeeds
kubectl argo rollouts status guestbook

# Show the rollout status
kubectl argo rollouts status guestbook --watch=false

# Watch the rollout until it succeeds, fail if it takes more than 60 seconds
kubectl argo rollouts status --timeout 60s guestbook

```

## Options

```
  -h, --help               help for status
  -t, --timeout duration   The length of time to watch before giving up. Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h). Zero means wait forever
  -w, --watch              Watch the status of the rollout until it's done (default true)
```

## Options inherited from parent commands

```
      --as string                      Username to impersonate for the operation. User could be a regular user or a service account in a namespace.
      --as-group stringArray           Group to impersonate for the operation, this flag can be repeated to specify multiple groups.
      --as-uid string                  UID to impersonate for the operation.
      --cache-dir string               Default cache directory (default "$HOME/.kube/cache")
      --certificate-authority string   Path to a cert file for the certificate authority
      --client-certificate string      Path to a client certificate file for TLS
      --client-key string              Path to a client key file for TLS
      --cluster string                 The name of the kubeconfig cluster to use
      --context string                 The name of the kubeconfig context to use
      --disable-compression            If true, opt-out of response compression for all requests to the server
      --insecure-skip-tls-verify       If true, the server's certificate will not be checked for validity. This will make your HTTPS connections insecure
  -v, --kloglevel int                  Log level for kubernetes client library
      --kubeconfig string              Path to the kubeconfig file to use for CLI requests.
      --loglevel string                Log level for kubectl argo rollouts (default "info")
  -n, --namespace string               If present, the namespace scope for this CLI request
      --request-timeout string         The length of time to wait before giving up on a single server request. Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h). A value of zero means don't timeout requests. (default "0")
  -s, --server string                  The address and port of the Kubernetes API server
      --tls-server-name string         Server name to use for server certificate validation. If it is not provided, the hostname used to contact the server is used
      --token string                   Bearer token for authentication to the API server
      --user string                    The name of the kubeconfig user to use
```

## See Also

* [rollouts](kubectl-argo-rollouts.md)	 - Manage argo rollouts
