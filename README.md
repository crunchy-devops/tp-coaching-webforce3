# tp-coaching-webforce3
Instruction pour la session de coaching
# TP ansible 1
Créer un fichier ansible-1.yaml qui automatise l'exercice 2 ci-dessus.

1-Le script doit mettre à jour les packages ubuntu.
2-Vérifier la version de python3
3-Créer un alias dans ~/.bashrc
4-installer le package pip
```
---
- name: Playbook exercice 1 ansible
  hosts: localhost
  become: true
  tasks:
   - name: Mise à jour les packages ubuntu
     ansible.builtin.apt:
             #name: update
      update_cache: yes
      upgrade: dist

   - name: vérifier la version de python3
     ansible.builtin.command:
      cmd: python3 --version

   - name: Créer un alias
     ansible.builtin.lineinfile:
      dest: ~/.bashrc
      line: 'alias python="python3"'
```
