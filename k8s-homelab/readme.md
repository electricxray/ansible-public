This will serve as the repo to manage the ansible plays and supporting files to create a home lab kubernets cluster.
An Ansible Vault will be used for the secrets portion in the context of Ansible and standing up the cluster. Hashicorp Vault will be used to within the context of k8s applications.
This is a project for me to expand my skills, expect some mistakes as I learn and develop.
Project Goal/Purpose: as close to an enterprise level K8s setup as I can reasonably maintain while maintaining my own life, with the goal of migrating other home lab services to this.
Rough environment mapping:
Hypervisor: Proxmox VE 9.
VM OS: RHEL 9, subject to change to RHEL 10 potentially for longevity and prevent a LEAPP process from being needed as early.
Kubernetes flavor: Vanilla, standard K8s.
GitOps functionality: ArgoCD
Registry: Harbor. I am not a developer, so this will come in more later on
Secrets management: HashiCorp Vault
Storage: Longhorn. Will be scalable. I don't have much storage currently, so being able to add will be a strong requirement which Longhorn meets.
Monitoring/observability/alerting: Prometheus/Grafana stack.
Infrastrucutre as Code: Ansible, until a shortcoming is identified.

I will be using IaC at all reasonably possible times.

Hardware being used: Dell R730xd. Dual socket E5 xeons, 12 physical cores each, hyperthreading enabled. 256GB DDR4 ECC Ram. 2-1TB MX500 SATA SSDs in RAID1 for OS storage, 1-1TB WD Blue disk in the front for other storage, to be upgraded.

Rough order of events:

1. Provision Proxmox on my server
