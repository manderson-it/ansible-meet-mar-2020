# Ansible Toronto March 2020 (virtual)

Also see https://www.meetup.com/Ansible-Toronto/events/269385291/

![Ansible Toronto March 2020 poster](./pics/AnsibleToronto_March31_11x17_SCREENVERSION.png "Ansible Toronto March 2020 poster")


## Requirements

- Export shell variables used by the playbooks.
- pip install pysnow
- SMTP server details (also exported as shell variables)

```bash
export SN_INSTANCE="devXXXXXX"
export SN_USERNAME="admin"
export SN_PASSWORD="yourPassword"

export MAIL_HOST="smtp.yourdomain.ca"
export MAIL_USERNAME="yourUsername"
export MAIL_PASSWORD="yourPassword"
```

## Run Playbooks

Playbooks are run on the Ansible controller.
Make sure you met the above requirements

```bash
ansible-playbook snow_cr_add_work_notes_with_email.yml
ansible-playbook snow_cr_get.yml
ansible-playbook snow_get_change_task.yml
ansible-playbook snow_get_change_tasks.yml
```
