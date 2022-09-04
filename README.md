# Telescope Organization Management

This repository contains tooling to support various orgaizational management capabilities for Project Telescope.

## GitHub Management

The configuration of the GitHub organization (repositories, teams and membership) is managed by [peribolos](https://github.com/kubernetes/test-infra/tree/master/prow/cmd/peribolos). The configuration for this organization is located in the [peribolos.yaml](peribolos.yaml) file at the root of this repository.

Changes are applied automatically with the help from the [peribolos-as-a-service](https://github.com/operate-first/peribolos-as-a-service) tool from the [Operate First](https://www.operate-first.cloud/) initiative.

## Quay Management

Container images assoicated with Project telescope are located within the Quay [telescope](https://quay.io/organization/telescope). The configuation including repositories, teams and robot accounts are managed in a declarative fashion within an Ansible inventory file located [here](ansible/inventory/group_vars/all.yml).

More information on the configuration parameters that can be employed can be found within the [quay Ansible Role](https://github.com/redhat-cop/infra-ansible/tree/main/roles/scm/quay) from the Red Hat Community of Practice (CoP).
