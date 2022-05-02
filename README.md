# asa-split_tunnel

#### Description

This playbook is used to update the split-tunnel configuration on ASAs.

#### Usage

* Clone the project
* Create a branch: `git checkout -b yourname`
* Edit **domains.yml** and add the domain you want to exclude from the tunnel. 
  * If you specify a root domain name, any sub-domain under it will be excluded. Example: `*.slack.com from .slack.com.`
  * Each line under the "domains" varible has a maximum of 500 characters. When the maximum is reached, you need to create a new line with a new list of domains. The previous line should always end with a "**,**" (comma)
* Check-in and push your branch changes: `git add --all ; git commit -m "my message"; git push origin yourname.`
* Follow the link it generates to create and submit a merge request. Once approved, the pipeline will run and update the ASAs with your list of domains.
