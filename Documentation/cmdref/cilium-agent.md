<!-- This file was autogenerated via cilium-agent --cmdref, do not edit manually-->

## cilium-agent

Run the cilium agent

### Synopsis


Run the cilium agent

```
cilium-agent
```

### Options

```
      --access-log string                 Path to access log of supported L7 requests observed
      --agent-labels stringSlice          Additional labels to identify this agent
      --allow-localhost string            Policy when to allow local stack to reach local endpoints { auto | always | policy }  (default "auto")
      --auto-ipv6-node-routes             Automatically adds IPv6 L3 routes to reach other nodes for non-overlay mode (--device) (BETA)
      --bpf-root string                   Path to BPF filesystem
      --config string                     Configuration file (default "$HOME/ciliumd.yaml")
      --container-runtime stringSlice     Sets the container runtime(s) used by Cilium { docker | none | auto }" (default [auto])
      --container-runtime-endpoint map    Container runtime(s) endpoint(s). (default: --container-runtime-endpoint=docker=unix:///var/run/docker.sock) (default map[])
  -D, --debug                             Enable debugging mode
      --debug-verbose stringSlice         List of enabled verbose debug groups
  -d, --device string                     Device facing cluster/external network for direct L3 (non-overlay mode) (default "undefined")
      --disable-conntrack                 Disable connection tracking
      --disable-ipv4                      Disable IPv4 mode
      --disable-k8s-services              Disable east-west K8s load balancing by cilium
  -e, --docker string                     Path to docker runtime socket (DEPRECATED: use container-runtime-endpoint instead) (default "unix:///var/run/docker.sock")
      --enable-policy string              Enable policy enforcement (default "default")
      --enable-tracing                    Enable tracing while determining policy (debugging)
      --envoy-log string                  Path to a separate Envoy log file, if any
      --ipv4-cluster-cidr-mask-size int   Mask size for the cluster wide CIDR (default 8)
      --ipv4-node string                  IPv4 address of node (default "auto")
      --ipv4-range string                 Per-node IPv4 endpoint prefix, e.g. 10.16.0.0/16 (default "auto")
      --ipv4-service-range string         Kubernetes IPv4 services CIDR if not inside cluster prefix (default "auto")
      --ipv6-node string                  IPv6 address of node (default "auto")
      --ipv6-range string                 Per-node IPv6 endpoint prefix, must be /96, e.g. fd02:1:1::/96 (default "auto")
      --ipv6-service-range string         Kubernetes IPv6 services CIDR if not inside cluster prefix (default "auto")
      --k8s-api-server string             Kubernetes api address server (for https use --k8s-kubeconfig-path instead)
      --k8s-kubeconfig-path string        Absolute path of the kubernetes kubeconfig file
      --keep-bpf-templates                Do not restore BPF template files from binary
      --keep-config                       When restoring state, keeps containers' configuration in place
      --kvstore string                    Key-value store type
      --kvstore-opt map                   Key-value store options (default map[])
      --label-prefix-file string          Valid label prefixes file path
      --labels stringSlice                List of label prefixes used to determine identity of an endpoint
      --lb string                         Enables load balancer mode where load balancer bpf program is attached to the given interface
      --lib-dir string                    Directory path to store runtime build environment (default "/var/lib/cilium")
      --log-driver stringSlice            Logging endpoints to use for example syslog, fluentd
      --log-opt map                       Log driver options for cilium (default map[])
      --logstash                          Enable logstash integration
      --logstash-agent string             Logstash agent address (default "127.0.0.1:8080")
      --logstash-probe-timer uint32       Logstash probe timer (seconds) (default 10)
      --masquerade                        Masquerade packets from endpoints leaving the host (default true)
      --nat46-range string                IPv6 prefix to map IPv4 addresses to (default "0:0:0:0:0:FFFF::/96")
      --pprof                             Enable serving the pprof debugging API
      --prefilter-device string           Device facing external network for XDP prefiltering (default "undefined")
      --prefilter-mode string             Prefilter mode { native | generic } (default: native) (default "native")
      --prometheus-serve-addr string      IP:Port on which to serve prometheus metrics (pass ":Port" to bind on all interfaces, "" is off)
      --restore                           Restores state, if possible, from previous daemon (default true)
      --single-cluster-route              Use a single cluster route instead of per node routes
      --socket-path string                Sets daemon's socket path to listen for connections (default "/var/run/cilium/cilium.sock")
      --state-dir string                  Directory path to store runtime state (default "/var/run/cilium")
      --trace-payloadlen int              Length of payload to capture when tracing (default 128)
  -t, --tunnel string                     Tunnel mode "vxlan" or "geneve" (default "vxlan")
      --version                           Print version information
```

