Ansible Role: DNS Configuration

This Ansible role is designed to automate the configuration of DNS (Domain Name System) settings on your target hosts. DNS is a crucial component of network infrastructure responsible for resolving domain names to IP addresses and vice versa.
Requirements

Before using this role, ensure you have the following prerequisites:

    Ansible is installed on your control machine.
    Access to the target hosts with the necessary privileges to modify DNS configuration files.

Role Variables

This role may require specific variables to be set based on your DNS configuration needs. These variables can be customized in your Ansible playbook to match your DNS server's configuration. Some common variables you might need to configure include:

    dns_server: The IP address or hostname of the DNS server.
    dns_search_domains: A list of search domains for DNS queries.
    dns_nameservers: A list of DNS nameservers to use for resolving DNS queries.

You can adjust these variables in your playbook's vars section.
Dependencies

This role does not have any dependencies on other Ansible roles.


Example Playbook

Here's an example playbook that demonstrates how to use this role:
---
- name: Configure DNS servers
  hosts: all
  become: yes
  vars:
    dns_servers:
      - 8.8.8.8
      - 78.88.8.8
  roles:
    - dns_configuration

License

This Ansible role is licensed under the MIT License. Feel free to modify and distribute it as needed for your projects.
