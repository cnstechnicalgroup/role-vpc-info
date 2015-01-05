Role: cns.vpc-info
========

This role gathers target VPC configuration information. It registers a playbook-global variable, vpc, for use in roles / tasks that require vpc related specifics.

Requirements
------------

Nothing, it runs out of the box.

Role Variables
--------------

In the current version, you can specify the following variables:

| Name               | Default |                                                                                                                                                                                           |
|--------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| vpc_cidr_block     |   ---   | The cidr block representing the VPC, e.g. 10.0.0.0/16                                                                                                                                     |
| vpc_resource_tags  |   ---   | A dictionary array of resource tags of the form: { tag1: value1, tag2: value2 }. Tags in this list are used in conjunction with CIDR block to uniquely identify a VPC in lieu of vpc_id.  |
| region             |   ---   | Region in which the resource exists.                                                                                                                                                      |

Dependencies
------------

This package has no dependencies.

License
-------

GPLv2

Author Information
------------------

Created by Sam Morrison
https://www.twitter.com/samcns

Examples
--------

```yaml
---
- name: common role test
  hosts: all
  roles:
    - cns.vpc-info
```
