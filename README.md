# This is to be used to Test the Custom Web Playbook

Running the playbook in Docker container with the
mapped host folder ./ansbile to /etc/ansible

```
mkdir -p ansible/tmp
git clone https://github.com/schogini/ansible-customeweb-playbook.git ansible/tmp/customweb
mv ansible/tmp/customweb-playbook.yml ansible/
docker run --rm -v $PWD/ansible:/etc/ansible schogini/docker-ansible-ws-ubuntu ansible-playbook /etc/ansible/customweb_playbook.yml
```