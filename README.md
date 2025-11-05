# exercice-algorithme-tableau-cryptage2

# Problème : (12 points)

On se propose de crypter un message composé par des mots séparés par un seul espace et ne contenant aucun signe de ponctuation (, ; . . ; ! ? ) en utilisant le principe suivant :

1) Placer chaque mot du message initial dans une case d'un tableau T. On suppose que le message est composé d'au maximum 20 mots.

2) Pour chaque élément du tableau T, ajouter autant de fois le caractère "*" pour que sa longueur sera égale à celle du mot le plus long dans le tableau T.

3) Dans un nouveau tableau T1 de taille N1 (N1=longeur du mot le plus long), répartir les lettres du mot se trouvant dans la case T[1] de façon à placer la lettre d'indice i du mot dans la case d'indice i du tableau T1.

4) Répartir de la même façon les lettres du mot contenu dans la case T[2] en concatérant à chaque fois la lettre d'indice i avec le contenu de la case i du tableau T1

5) Répartir de la même façon le reste des mots de T dans T1.

6) Concatérer les mots obtenus dans T1 en les séparant par un espace pour obtenir le message crypté.

**Exemple :** Si le message à crypter est "Bonjour Sami j'ai fini mon travail", les étapes de cryptage sont :

**Etape 1 :** Répartir les mots du message dans le tableau T :

| T= | Bonjour | Sami | j'ai | fini | mon | travail |

 

N=6
| Step | T1[0]   | T1[1]   | T1[2]   | T1[3]   | T1[4]   | T1[5]   | T1[6]   |
|------|---------|---------|---------|---------|---------|---------|---------|
| T[0] | B       | o       | n       | j       | o       | u       | r       |
| T[1] | BS      | oa      | nm      | ji      | o*      | u*      | r*      |
| T[2] | BSj     | oa'     | nma     | jii     | o**     | u**     | r**     |
| T[3] | BSjf    | oa'i    | nman    | jiii    | o***    | u***    | r***    |
| T[4] | BSjfm   | oa'io   | nmann   | jiii*   | o****   | u****   | r****   |
| T[5] | BSjfmt  | oa'ior  | nmanna  | jiii*v  | o****a  | u****i  | r****l  |
# Le message crypté sera alors "BSjfmt oa'ior nmanna jiii*v o****a u****i r****i"
