# BlueCatAddressManagerNetworkFacts
An Ansible playbook that uses the BlueCat Address Manager API and creates human readable reports about all networks from the RESTful response

## Written by John Capobianco

Using the BAM API this playbook first gathers facts and then saves RAW JSON, Nice JSON, Nice YAML, CSV, Markdown, and interactive HTML Mind Map files from the returned stateful data. 

### Prerequisites

1) Install Ansible

    $ pip install --user ansible

    Centos:

    yum install python

    yum install ansible

2) Check version of Ansible

    $ansible --version

    ansible 2.9.1

3) Install node.js and npm

curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -

4) Clone the Repository

    git clone https://github.com/automateyournetwork/BlueCatAddressManagerNetworkFacts.git

### Run the playbook

After updating the hosts file with the proper hostnames run the playbook.

cd BlueCatAddressManagerNetworkFacts.git

cd playbooks

ansible-playbook GetBAMNetworks.yml

<answer prompts for credentials> 

<playbook gathers facts>

<playbook creates files>

cd ..

cd documentation/BAM

ls

Review files

### Output files

The following files are created per host:

Network Facts

Network_Facts_RAW.json - ALL RAW JSON returned data

Network_Facts_Nice.json - All JSON returned data filtered to Nice JSON

Network_Facts.yml - All returned data in Nice YAML

Network_Facts.csv - Fields in CSV

Network_Facts.md - Fields in Markdown

Network_Facts.html - Fields interactive HTML mind map

#### DEVELOPMENT NOTES

Developed with VS Code, Ansible, CentOS
