# Enketo Local Update

Added this repo because I got tired of updating my local enketo-express repo manually ;-)


## Getting started
1. [Install ansible](http://docs.ansible.com/ansible/latest/intro_installation.html)
    > NB: tested with ansible 2.4.0.0
2. Create a new file called `localhost` in `host_vars` directory then copy the contents in `default-localhost` to the new file you have created.
3. Update the following variables in the new file:

    - `enketo_path <string>` - path where you want enketo to reside
    - `enketo_remote <string>` - path to remote enketo repo
    - `git_path <string>` - your git path locally. I used `which git` from a mac
    - `git_branch <string>` - branch that should be updated
    - `should_rebase <boolean>` - rebase with latest tag branch or not

4. Run `ansible-playbook -i hosts -vvv main.yaml`