# Ansible-automated-EC2-SSHKeyAdding
Astuce simple pour ajouter plusieurs clé publique à une instance EC2 en utilisant ansible. 

1 - Mettre en place les serveurs que vous voulez cibler sous le fichiers ansble_hosts (Ajouter les addresses IP)

2 - Ajouter dans le dossier cloné les fichiers des clé publiques que vous voulez ajouter aux serveurs

3 - Lancer la commande (En changeant avec vos paramétres et vos paths) :  $ansible-playbook /Ansible-automated-EC2-SSHKeyAdding/add-key.yml -i /Ansible-automated-EC2-SSHKeyAdding/ansible_hosts --user ubuntu --key-file /Path/Pour/Votre_clé_privée.pem -e "key=~/.ssh/id_rsa.pub" 
