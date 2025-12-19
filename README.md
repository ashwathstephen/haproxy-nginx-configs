# HAProxy and Nginx Configurations

[![HAProxy](https://img.shields.io/badge/HAProxy-2.8+-004C9B)](https://www.haproxy.org/)
[![Nginx](https://img.shields.io/badge/Nginx-1.25+-009639?logo=nginx)](https://nginx.org/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Production-ready HAProxy and Nginx configurations for load balancing, reverse proxy, and traffic management. Includes zero-downtime reload patterns and SSL termination.

## Features

- High-availability load balancing
- Zero-downtime configuration reloads
- SSL/TLS termination with modern cipher suites
- Rate limiting and connection limits
- Health checks and failover
- Logging and monitoring integration
- Kubernetes ingress patterns

## HAProxy Configurations

| Config | Use Case |
|--------|----------|
| haproxy.cfg | Production load balancer |
| haproxy-k8s.cfg | Kubernetes ingress controller |
| haproxy-tcp.cfg | TCP/Layer 4 load balancing |

## Nginx Configurations

| Config | Use Case |
|--------|----------|
| nginx.conf | Base configuration |
| reverse-proxy.conf | API gateway/reverse proxy |
| static-files.conf | Static file serving |
| ssl-termination.conf | HTTPS termination |

## Testing

```bash
# Validate HAProxy config
haproxy -c -f haproxy/haproxy.cfg

# Validate Nginx config
nginx -t -c nginx/nginx.conf

# Reload without downtime
kill -USR2 $(cat /var/run/haproxy.pid)
nginx -s reload
```

## Author

Ashwath Abraham Stephen
Senior DevOps Engineer | [LinkedIn](https://linkedin.com/in/ashwathstephen) | [GitHub](https://github.com/ashwathstephen)

## License

MIT License - see [LICENSE](LICENSE) for details.

