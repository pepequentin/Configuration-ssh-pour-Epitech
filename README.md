# Configuration-ssh-pour-Epitech
Rappel / Tuto pour configurer son ssh avec blih epitech

Si vous avez ce genre d'erreur : git@git.epitech.eu: Permission denied (publickey).

fatal: Impossible de lire le dépôt distant.

Il y a une solution, en 3 étapes.

1. Déjà, il faut vous assurez que vous avez une clé ssh si non -> ssh-keygen -t rsa

2. Envoyé la clé à blih -> blih -u "prenom.nom@epitech.eu" sshkey upload ~/.ssh/id_rsa.pud

3. Définir le type de hachage -> eval "$(ssh-agent -s)"
                              -> ssh-add -l -E md5
                              
Après c'est good :)
