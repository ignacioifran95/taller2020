# Playbook de Ansible: Proxy reverso con balanceo de carga

Playbook de ansible para instalar apache y proxy reverso con balanceo de carga para RHEL/CentOS y Debian/Ubuntu

## Ejecución:


`$ ansible-playbook main.yml -i inventario --ask-become-pass`

## Roles:

El playbook ejecutará las tareas correspondientes según la familia de SO de los servidores que estén en el inventario.
En este caso tenemos 2 roles, apache-centos y apache-debian.

## Templates

La configuración de los virtual host con la configuración de proxy y balanceo de carga se copiará desde un template loadbalancer.j2
que se encuentra en el directorio templates/ de cada rol.

Los templates serán configurados mediante variables que se encuentran definidas en el archivo loadbalancer_vars.yml 
