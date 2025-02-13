Pour répartir tous les tubes et doses pour chaque membre de l'équipe et remplir le tableau dans `Feuil2`, nous devons suivre une approche méthodique. Voici comment procéder étape par étape :

### Étapes de Répartition

1. **Calcul du Total des Médecins Couverts** :
    - Additionner le nombre total de médecins couverts par tous les délégués.
    
2. **Calcul du Total d'Échantillons Nécessaires** :
    - Chaque médecin doit recevoir 6 tubes différents et 6 doses (réparties en 3+3).
    - Multiplier le total des médecins par 6 pour obtenir le total de tubes et doses nécessaires.

3. **Répartition Proportionnelle des Tubes et Doses** :
    - Diviser les tubes et doses disponibles proportionnellement au nombre de médecins couverts par chaque délégué.

### Formules Utilisées

#### Feuil2 : Calculs Préliminaires
- **Total Médecins Couverts** : 
    ```excel
    =SUM(B2:B7)
    ```
- **Total Tubes/Doses Nécessaires** : 
    ```excel
    =Total_Médecins_Couverts * 6
    ```

#### Feuil2 : Attribution aux Délégués
- **Tubes/Doses Attribués par Délégué** : 
    ```excel
    =ROUND((Nombre_Médecins_Délégué / Total_Médecins_Couverts) * Quantité_Disponible, 0)
    ```

### Exemple de Répartition dans Excel

Voici un exemple de la manière dont remplir chaque cellule pour chaque type de tube/dose :

| Délégué | Nombre Médecins | SULFUR 15CH DOSES | FOLLICULINUM 15CH DOSES | GELSEMIUM 30CH DOSES | SILICEA 15CH DOSES | ... |
|---------|-----------------|-------------------|-------------------------|-----------------------|---------------------|-----|
| Rahma   | 73              | =ROUND((B2/$B$8)*Feuil1!C2, 0) | =ROUND((B2/$B$8)*Feuil1!C3, 0) | =ROUND((B2/$B$8)*Feuil1!C4, 0) | =ROUND((B2/$B$8)*Feuil1!C5, 0) | ... |
| Ahmed B | 76              | =ROUND((B3/$B$8)*Feuil1!C2, 0) | =ROUND((B3/$B$8)*Feuil1!C3, 0) | =ROUND((B3/$B$8)*Feuil1!C4, 0) | =ROUND((B3/$B$8)*Feuil1!C5, 0) | ... |
| Nizar   | 53              | =ROUND((B4/$B$8)*Feuil1!C2, 0) | =ROUND((B4/$B$8)*Feuil1!C3, 0) | =ROUND((B4/$B$8)*Feuil1!C4, 0) | =ROUND((B4/$B$8)*Feuil1!C5, 0) | ... |
| Houssem | 203             | =ROUND((B5/$B$8)*Feuil1!C2, 0) | =ROUND((B5/$B$8)*Feuil1!C3, 0) | =ROUND((B5/$B$8)*Feuil1!C4, 0) | =ROUND((B5/$B$8)*Feuil1!C5, 0) | ... |
| Taher   | 94              | =ROUND((B6/$B$8)*Feuil1!C2, 0) | =ROUND((B6/$B$8)*Feuil1!C3, 0) | =ROUND((B6/$B$8)*Feuil1!C4, 0) | =ROUND((B6/$B$8)*Feuil1!C5, 0) | ... |
| Ahmed A | 60              | =ROUND((B7/$B$8)*Feuil1!C2, 0) | =ROUND((B7/$B$8)*Feuil1!C3, 0) | =ROUND((B7/$B$8)*Feuil1!C4, 0) | =ROUND((B7/$B$8)*Feuil1!C5, 0) | ... |

### Instructions Pas à Pas

1. **Calculer le Total des Médecins Couverts** :
    - Dans la cellule `B8` de `Feuil2`, insérez la formule :
        ```excel
        =SUM(B2:B7)
        ```

2. **Attribution des Tubes/Doses** :
    - Pour chaque cellule correspondant à un type de tube ou dose pour chaque délégué, utilisez la formule donnée ci-dessus. Par exemple, pour attribuer les "SULFUR 15CH DOSES" à Rahma :
        ```excel
        =ROUND((B2/$B$8)*Feuil1!C2, 0)
        ```
    - Copiez cette formule pour toutes les autres cellules correspondantes en ajustant les références de cellules selon le besoin.

3. **Vérification** :
    - Assurez-vous que la somme des quantités attribuées pour chaque type de tube/dose ne dépasse pas la quantité disponible dans `Feuil1`.

### Résultat Final

Le résultat final sera un tableau complètement rempli avec la répartition proportionnelle des tubes et doses pour chaque délégué, respectant ainsi les critères définis.

Si vous avez accès à Google Sheets ou Microsoft Excel Online, je peux vous aider à créer ce fichier directement et vous fournir un lien partagé si nécessaire.
