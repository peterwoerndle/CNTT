[<< Back](../../openstack)

# 5. Interfaces and APIs
<p align="right"><img src="../figures/bogo_ifo.png" alt="scope" title="Scope" width="35%"/></p>

## Table of Contents
* [5.1 Introduction](#5.1)
* [5.2 Core OpenStack Services APIs](#5.2)
* [5.3 Consolidated Set of APIs](#5.3)

<a name="5.1"></a>
## 5.1 Introduction

This chapter presents a consolidated set of OpenStack Service APIs corresponding to the ETSI NFV Vi-Vnfm and Or-Vi interfaces.
The OpenStack Pike version is used as the baseline for these APIs and CLIs. CNTT reference architectures and future
reference implementations will only considered OpenStack releases greater or equal to Pike. Any reference
implementation that **get certified by RC** can be considered as CNTT RA Compliant. When different OpenStack version
based reference implementations gets certified then the "CNTT standard" will be the oldest used OpenStack release.
Example, Let us assume that the Pike, Queens and Stein OpenStack based reference implementations get certified. Then,
the CNTT standard OpenStack version will be Pike.

The Chapter presents the APIs for the core OpenStack services defined in Chapter 3 and later in the Chapter a
consolidated view of these and other APIs that would be of interest.

<a name="5.2"></a>
## 5.2. Core OpenStack Services APIs

### 5.2.1. Keystone

| **OpenStack Service** | **API Version** |
|-----------------------|-----------------|
| Identity: Keystone    | 3.8             |

| **Keystone Features**   | **Mandatory** |
|-------------------------|:-------------:|
| application_credentials | X             |
| external_idp            |               |
| federation              |               |
| project_tags            | X             |
| security_compliance     | X             |
| trust                   | X             |

Identity API v3: https://docs.openstack.org/api-ref/identity/v3/index.html

Identity API v3 extensions: https://docs.openstack.org/api-ref/identity/v3-ext/

Security compliance and PCI-DSS: https://docs.openstack.org/keystone/train/admin/configuration.html#security-compliance-and-pci-dss

### 5.2.2 Glance

| **OpenStack Service** | **Minimal API Version** |
|-----------------------|-------------------------|
| Image: Glance         | 2.5                     |

Image Service Versions: https://docs.openstack.org/api-ref/image/versions/index.html#version-history

### 5.2.3. Cinder

| **OpenStack Service** | **Version** | **Minimal Microversion** |
|-----------------------|-------------|--------------------------|
| Block Storage: Cinder | 3           | 3.43                     |

| **Cinder Features**    | **Mandatory** |
|------------------------|:-------------:|
| backup                 | X             |
| clone                  | X             |
| consistency_group      |               |
| extend_attached_volume |               |
| manage_snapshot        | X             |
| manage_volume          | X             |
| snapshot               | X             |
| volume_revert          | X             |

Block Storage API: https://docs.openstack.org/api-ref/block-storage/

REST API Version History: https://docs.openstack.org/cinder/latest/contributor/api_microversion_history.html

### 5.2.4. Swift

| **OpenStack Service** | **API Version** |
|-----------------------|-----------------|
| Object Storage: Swift | 1               |

| **Swift Features** | **Mandatory** |
|--------------------|:-------------:|
| account_quotas     | X             |
| bulk_delete        | X             |
| bulk_upload        | X             |
| container_quotas   | X             |
| container_sync     | X             |
| crossdomain        | X             |
| discoverability    | X             |
| form_post          | X             |
| ratelimit          | X             |
| s3api              |               |
| slo                | X             |
| staticweb          | X             |
| symlink            | X             |
| temp_url           | X             |
| tempauth           | X             |
| versioned_writes   | X             |

Object Storage API: https://docs.openstack.org/api-ref/object-store/index.html

Discoverability: https://docs.openstack.org/swift/latest/api/discoverability.html

### 5.2.5. Neutron

| **OpenStack Service** | **Link for API and CLI** | **API/CLI Minimum (Baseline) Version** |
|------------------|----------------------------------------------------|-------------------|
| Networking: Neutron | https://docs.openstack.org/api-ref/network/ | Version 2.0 |
| Networking: Neutron | https://docs.openstack.org/python-neutronclient/latest/cli/index.html | Version 2.0 |

| **Neutron Extensions**         | **Mandatory** |
|--------------------------------|:-------------:|
| address-scope                  | X             |
| agent                          | X             |
| allowed-address-pairs          | X             |
| auto-allocated-topology        | X             |
| availability_zone              | X             |
| availability_zone_filter       | X             |
| binding                        | X             |
| binding-extended               | X             |
| default-subnetpools            | X             |
| dhcp_agent_scheduler           | X             |
| dns-domain-ports               |               |
| dns-integration                |               |
| dvr                            | X             |
| empty-string-filtering         | X             |
| ext-gw-mode                    | X             |
| external-net                   | X             |
| extra_dhcp_opt                 | X             |
| extraroute                     | X             |
| flavors                        | X             |
| filter-validation              | X             |
| fip-port-details               | X             |
| floatingip-pools               |               |
| ip-substring-filtering         | X             |
| l3_agent_scheduler             | X             |
| l3-flavors                     | X             |
| l3-ha                          | X             |
| logging                        |               |
| metering                       |               |
| multi-provider                 | X             |
| net-mtu                        | X             |
| net-mtu-writable               | X             |
| network_availability_zone      | X             |
| network-ip-availability        | X             |
| network-segment-range          |               |
| pagination                     | X             |
| port-mac-address-regenerate    | X             |
| port-resource-request          |               |
| port-security                  | X             |
| port-security-groups-filtering | X             |
| project-id                     | X             |
| provider                       | X             |
| rbac-policies                  | X             |
| router                         | X             |
| router_availability_zone       | X             |
| qos                            | X             |
| qos-bw-limit-direction         | X             |
| qos-bw-minimum-ingress         | X             |
| qos-default                    | X             |
| qos-fip                        | X             |
| qos-gateway-ip                 | X             |
| qos-rule-type-details          | X             |
| qos-rules-alias                | X             |
| quotas                         | X             |
| quota_details                  | X             |
| revision-if-match              | X             |
| security-group                 | X             |
| service-type                   | X             |
| sorting                        | X             |
| standard-attr-description      | X             |
| standard-attr-revisions        | X             |
| standard-attr-tag              | X             |
| standard-attr-timestamp        | X             |
| subnet_allocation              | X             |
| subnet-service-types           | X             |
| rbac-security-groups           |               |
| router-interface-fip           |               |
| trunk                          | X             |
| trunk-details                  | X             |
| uplink-status-propagation      |               |

The exhaustive list of extensions is available at https://docs.openstack.org/api-ref/network/v2/

### 5.2.6. Nova

| **OpenStack Service** | **API Version** | **Minimal Microversion** |
|-----------------------|-----------------|--------------------------|
| Compute: Nova         | 2.1             | 2.53                     |

| **Nova Features**        | **Mandatory** |
|--------------------------|:-------------:|
| attach_encrypted_volume  |               |
| change_password          |               |
| cold_migration           | X             |
| console_output           | X             |
| disk_config              | X             |
| interface_attach         | X             |
| live_migration           | X             |
| metadata_service         | X             |
| pause                    | X             |
| personality              |               |
| rdp_console              |               |
| rescue                   | X             |
| resize                   | X             |
| serial_console           |               |
| shelve                   | X             |
| snapshot                 | X             |
| spice_console            |               |
| suspend                  | X             |
| swap_volume              |               |
| vnc_console              |               |
| volume_multiattach       |               |

Compute API: https://docs.openstack.org/api-ref/compute/

REST API Version History: https://docs.openstack.org/nova/latest/reference/api-microversion-history.html

### 5.2.7. Heat

|**OpenStack Service** | **Link for API and CLI** | **API/CLI Minimum (Baseline) Version** |
|------------------|----------------------------------------------------|-------------------|
| Bare Metal: Heat | https://docs.openstack.org/api-ref/orchestration/v1/index.html#api-versions | Version 1.0 |
| Bare Metal: Heat | https://docs.openstack.org/python-heatclient/latest/ | Version 1.25 |


<a name="5.3"></a>
## 5.3. Consolidated Set of APIs

### 5.3.1. OpenStack Interfaces
This section illustrates some of the Interfaces provided by OpenStack; the exhaustive list of APIs is available
at https://docs.openstack.org/api-ref/.

OpenStack REST APIs are simple to interact with using either of two options. Clients can either call the APIs
directly using the HTTP or REST library, or they can use one of the many programming language specific cloud
libraries.

**APIs**

| OpenStack Service | Link for API list | API Minimum (Baseline) Version |
|------------------|--------------------|------------------------|
| Identity: Keystone | https://docs.openstack.org/api-ref/identity/v3/index.html?expanded=#identity-api-operations  | Version 3.10 |
| Compute: Nova | https://docs.openstack.org/api-ref/compute/  | Version 2.1 |
| Networking: Neutron | https://docs.openstack.org/api-ref/network/  | Version 2.0 |
| Imaging: Glance | https://docs.openstack.org/api-ref/image/v2/index.html#images  | Version 2.0 |
| Block Storage: Cinder | https://docs.openstack.org/api-ref/block-storage/v3/index.html#api-versions  | Version 3.0 |
| Object Storage: Swift | https://docs.openstack.org/api-ref/object-store/  | Version 1.0 |
| Orchestration: Heat | https://docs.openstack.org/api-ref/orchestration/v1/index.html#api-versions  | Version 1.0 |
| Acceleration: Cyborg | https://docs.openstack.org/api-ref/accelerator/v1/index.html  | Version 1.0 |

**CLIs**

| OpenStack Service | Link to Client | Client Minimum (Baseline) Version |
|------------------|--------------------|------------------------|
| Identity: Keystone | https://docs.openstack.org/python-keystoneclient/latest/using-api-v3.html | Version 3.10 |
| Compute: Nova | https://docs.openstack.org/python-novaclient/latest/cli/index.html | Version 2.1 |
| Networking: Neutron | https://docs.openstack.org/python-neutronclient/latest/cli/index.html | Version 2.0 |
| Imaging: Glance | https://docs.openstack.org/python-glanceclient/latest/ | Version 2.0 |
| Block Storage: Cinder | https://docs.openstack.org/python-cinderclient/latest/ | Version 3.0 |
| Object Storage: Swift | https://docs.openstack.org/python-swiftclient/latest/ | Version 1.0 |
| Orchestration: Heat | https://docs.openstack.org/python-heatclient/latest/ | Version 1.0 |
| Acceleration: Cyborg | https://docs.openstack.org/python-cyborgclient/latest/ | Version 1.0 |
| OpenStack Client (python) | https://docs.openstack.org/python-openstackclient/pike/index.html  | Version 3.2.1 |

### 5.3.2. Kubernetes Interfaces
The Kubernetes APIs are available at https://kubernetes.io/docs/concepts/overview/kubernetes-api/.

### 5.3.3. KVM Interfaces
The KVM APIs are documented in Section 4 of the document https://www.kernel.org/doc/Documentation/virtual/kvm/api.txt.

#### 5.3.3.1. Libvirt Interfaces
The Libvirt APIs are documented in https://libvirt.org/html/index.html.

<!--
### 5.3.4. vSphere/ESXi APIs
The ESXi APIs are documented together with vCenter and available at https://code.vmware.com/apis/62/vcenter-management
-->
