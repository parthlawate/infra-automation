# Automating Common IT Infra Tasks
Repo that contains scripts to automate various infrastructure activities like developer workstation setup and configuration. 

## Setting up User Workstations
User workstations can be set up with the required development tools by running the following command in a terminal. Needs to be run by a user with sudo access

```bash
sudo mkdir -p /tmp/ansible-ttpl-it-automation && sudo wget -q "https://gist.githubusercontent.com/coolbung/2624e103156f7b790791/raw/ttpl_install.sh" -O /tmp/ansible-ttpl-it-automation/ttpl_install.sh && sudo chmod +x /tmp/ansible-ttpl-it-automation/ttpl_install.sh && sudo /tmp/ansible-ttpl-it-automation/ttpl_install.sh
```
The script will set up all the tools defined in the `environment-setup.yml` file and also set up 2 vhosts, one each for PHP5 & PHP7

- To access the PHP5 localhost, navigate to http://machineusername-php5.local/  Eg: http://ttpl21-php5.local/
- To access the PHP7 localhost, navigate to http://machineusername-php7.local/  Eg: http://ttpl21-php7.local/
- The files for this are present in /var/www/ttpl21-php5.local/public or in /var/www/ttpl21-php7.local/public
- PHP My Admin is not installed, so you can download Adminer (http://adminer.org/) and place the file anywhere in your local
