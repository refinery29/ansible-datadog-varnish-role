# An Ansible role to setup and configure the Varnish integration for the Datadog Agent
The Datadog.datadog role maintained by Datadog is great, but it does not attempt to configure
monitored services for monitoring, and in order to have it configure multiple integrations, you
would either have to duplicate your configs a lot, or do tricky things with Ansible variables
which you shouldn't be doing and aren't worth your time.

This role provides an alternate way to setup a target machine and its Datadog agent to monitor
Varnish.

## Installation

It is strongly recommended that the [Datadog.datadog role][] is used to install the agent.

With the agent installed, this role may be run with become if everything is default (at least on ubuntu 14.04).

The datadog agent's username and group may be configured, as well as the integration's tags as well as the entire config.

Consult this role's [defaults](defaults/main.yml) for variables names.

[Datadog.datadog role]: https://github.com/DataDog/ansible-datadog
