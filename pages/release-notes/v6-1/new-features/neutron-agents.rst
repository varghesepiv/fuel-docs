
Neutron agents state reporting
------------------------------

Mirantis OpenStack 6.1 has obtained its own logic to determine
if agents are dead or alive. Agents do not need to use
REST API calls anymore to notify a neutron server
which maintains agents' state by collecting state
reports from agents via AMQP. They can report their
own status by saving it in local files.
So, when a message queue has issues the Cluster Resource Manager
still can response in time if something goes
wrong with an agent.

See the `blueprint
<https://blueprints.launchpad.net/fuel/+spec/neutron-agents-local-reports>`_
for details about the implementation.
