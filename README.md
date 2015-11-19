A playbook to **install/upgrade/downgrade aerospike** server along with **asgraphite** (aerospike's metrics graphite reporting tool)

How to run:

deployment (you will be prompted for aerospike enterprise user and pass):

```ansible-playbook -i production --limit 2.2.2.1,2.2.2.2 aerospike.yml -u root --ask-pass```

to debug templates use --check --diff --limit and also uncomment always_run clause where needed:

```ansible-playbook -i production --check --diff --limit 2.2.2.1 aerospike.yml -u root --ask-pass```


note that common role is most probably not needed or can be significantly reduced, up to couple of steps, so it needs to be tested on fresh machine and cleaned up

