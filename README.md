# Ansible Role: Cassandra

[![Build Status](https://travis-ci.org/davey-dev/ansible-role-cassandra.svg?branch=master)](https://travis-ci.org/davey-dev/ansible-role-cassandra)

Installs [Cassandra](http://cassandra.apache.org/) on Debian/Ubuntu.

## Requirements

Debian/Ubuntu

## Role Variables

    cluster_name: 'My Cluster'

The name of the cluster. This is mainly used to prevent machines in one logical cluster from joining another.

    batch_size_warn_threshold_in_kb: 50

Log WARN on any batch size exceeding this value. 5kb per batch by default.
Caution should be taken on increasing the size of this threshold as it can lead to node instability.

    batch_size_fail_threshold_in_kb: 500

Fail any batch exceeding this value. 50kb (10x warn threshold) by default.


## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - { role: davey-dev.cassandra }

## License

MIT / BSD

## Author Information

This role was created in 2016 by Dave Gallant
