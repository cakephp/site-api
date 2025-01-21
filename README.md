This repository is published as a dokku application that handles `api.cakephp.org`.

The primary function of this is to create an nginx instance that handles proxying requests to the various versions of the API docs that are published.
Each of these servers has separate `location` directives that unify the URL space.

The `web.py` script is used to trick dokku into having a process to monitor.

# Deployment

This application is deployed on each push to `master`. Deployment is handled by GitHub Actions.
