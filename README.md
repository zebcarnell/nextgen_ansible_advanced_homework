Role Name
=========

Playbooks to setup ansible tower, then use CI/CD processes to deploy a QA environment with a 3 tier app and if successful deploy a production environment with the 3 tier app.

Requirements
------------

Requirements deployed as part of playbook.


Role Variables
--------------

```yaml
tower_GUID= #GUID for tower environment
osp_GUID= #GUID for OpenStack environment
osp_DOMAIN= #Domain for OpenStack environment
opentlc_login= #Your Red Hat Open TLC login
path_to_opentlc_key= #Path to your private key for Open TLC login
param_repo_base= #JQ Repo Base
opentlc_password= #Your Open TLC Password 
REGION_NAME= #The AWS region you will deploy your prod environment too. I.E: us-east-1
EMAIL= #Your email address
github_repo= #Path to your github repo for use in provisioning servers and apps
```


Dependencies
------------

None


Usage
----------------
Example:

```bash
ansible-playbook site-3tier-app.yml -e tower_GUID=${TOWER_GUID} -e osp_GUID=${OSP_GUID} -e osp_DOMAIN=${OSP_DOMAIN} -e opentlc_login=${OPENTLC_ID} -e path_to_opentlc_key=/root/.ssh/mykey.pem -e param_repo_base=${JQ_REPO_BASE} -e opentlc_password=${OPENTLC_PASSWORD} -e REGION_NAME=${REGION} -e EMAIL=${MAIL_ID} -e github_repo=${GITHUB_REPO}
```

License
-------

BSD

Author Information
------------------

Zeb Carnell
