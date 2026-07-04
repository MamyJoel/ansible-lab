# Ansible Lab

Lab personnel d'automatisation avec Ansible sur infrastructure Linux.

## Stack technique
- **Control node** : Ubuntu 20.04
- **Managed node** : Ubuntu 20.04
- **Ansible** : 2.13.x

## Structure

ansible-lab/
├── ansible.cfg
├── site.yml
├── inventory/
│   └── inventory.ini
└── roles/
└── nginx/
├── tasks/main.yml
├── handlers/main.yml
├── files/
└── templates/


## Prérequis
- Authentification SSH par clé entre control node et managed nodes
- Python 3 sur les managed nodes

## Utilisation

```bash
# Lancer le déploiement complet
ansible-playbook -i inventory/inventory.ini site.yml

# Tester la connectivité
ansible -i inventory/inventory.ini targets -m ping
```

## Rôles disponibles
| Rôle  | Description |
|-------|-------------|
| nginx | Installation, configuration et déploiement nginx |

