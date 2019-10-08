1. Clone github repo:

     git clone git@github.com:vpryimak/python_app.git

2. Change directory:

   cd python_app

3. Modify file hosts and put your server external ip address

4. Execute ansible playbook
 
   ansible-playbook --private-key=/your_path_to_private_key/your_private_key_name.pem -i hosts playbook-app.yml

5. Open http://external_ip_address and see message - "Hello World!"

6. How to check postgres user and password:
   Connect to instance via ssh and execute command: psql -U my_app  -h localhost -d my_app_db -W
   
   Postgres dbname - my_app_db, user - my_app, pass - my_app. 

Ansible playbook tested on AWS(Ubuntu Server 18.04). Default user for this OS(ubuntu) which set in playbook-app.yml. 