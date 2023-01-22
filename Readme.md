# Ansible role YSA.OAuth2-Proxy

# Description
Installing and configuring [OAuth2 Proxy](https://github.com/oauth2-proxy/oauth2-proxy)

# Configuration

```yaml
---
# Version for installing
oauth2_proxy_version: '7.4.0'

# For multiarch or multios installation need set to 'false' for get checksum each host
# because checksums are stored separately for each release file
# by default, supposing that installation carried to mono-arch/os hosts and get one checksum for all
oauth2_proxy_get_checksum_once: true

# System user
oauth2_proxy_user: 'oauth2-proxy'
oauth2_proxy_group: 'oauth2-proxy'

# Directories
oauth2_proxy_install_dir: '/opt/oauth2-proxy'
oauth2_proxy_config_path: '{{ oauth2_proxy_install_dir }}/oauth2-proxy.conf'

# Systemd service
oauth2_proxy_service_name: 'oauth2-proxy'

# Configuration
oauth2_proxy_backup_config_before_change: true
oauth2_proxy_config: 
  - see: https://oauth2-proxy.github.io/oauth2-proxy/docs/configuration/overview

```