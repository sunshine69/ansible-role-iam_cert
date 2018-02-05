iam_cert
=========

Given a `cert` as a list of dict with key name is the same as the parameter name of the ansible module iam_cert, handle aws certificate operation.

If `profile` is not given using an assume role `upload_iam_cert_role_arn` to get permissions if possible. 
 
Requirements
------------


Role Variables
--------------

`certs` - optional - default: []
 List of certs as a dict to create/delete
`stage` - optional - default: 'create' 
 action to do
`upload_iam_cert_role_arn` - optional - no default
 The role name that the current ec2 iam role can assume in order to do the operations.
 This is for running on ci agent, the agent IAM role should be given the right to assume the remote role. 

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
