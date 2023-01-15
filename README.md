Role Vector
=========

Requirements
------------
Для установки роли создайте 'requirements.yml'
```
  - name: vector_role
    src: git@github.com:chernykhal/vector-role.git
    scm: git
    version: "[last version]"
```

Role Variables
--------------

[defaults/main.yml](./defaults/main.yml) - изменяемые параметры;

[tasks/download](./tasks/download) - получение дистрибутива Vector;

[tasks/install](./tasks/install) - установка дистрибутива; 

[tasks/configure.yml](./tasks/configure.yml) - развертывание конфига Vector

[tasks/main.yml](./tasks/main.yml) - play установки Vector

[vars/main.yml](./vars/main.yml) - постоянные параметры для сервиса Vector;

Example usage:
----------------
```
- name: Install Vector
  hosts: vector
  roles:
    - vector_role
```
-------
