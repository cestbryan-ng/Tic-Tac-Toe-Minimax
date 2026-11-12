# Tic-Tac-Toe avec Minimax

Jeu de Tic-Tac-Toe sur une grille de 3 × 3, où un joueur humain affronte une IA. L'IA choisit ses coups avec l'algorithme **Minimax** et l'**élagage alpha-bêta** : elle explore les suites possibles de la partie et évite d'examiner certaines branches qui ne peuvent pas améliorer le résultat.

## Interface du runner

![Interface du jeu de Tic-Tac-Toe](assets/images/runner-interface.png)

## Fonctionnalités

- Choix de jouer avec `X` ou `O`.
- Réponse automatique de l'IA après chaque coup du joueur.
- Détection de victoire, de défaite ou de match nul.
- Possibilité de recommencer une partie.

## Comment jouer

1. Lancez le jeu et choisissez **Play as X** ou **Play as O**.
2. Cliquez sur une case vide pour jouer votre symbole.
3. L'IA joue automatiquement avec l'autre symbole.
4. Quand la partie est terminée, cliquez sur **Play Again** pour recommencer.

`X` commence toujours la partie. Une ligne horizontale, verticale ou diagonale de trois symboles identiques remporte la partie. Si la grille est pleine sans alignement gagnant, la partie est nulle.

## Algorithme de l'IA

Minimax évalue les issues possibles : une victoire de `X` vaut `1`, une victoire de `O` vaut `-1` et un match nul vaut `0`. Le joueur `X` cherche à maximiser le score, tandis que `O` cherche à le minimiser. L'élagage alpha-bêta accélère cette recherche en supprimant les branches qui ne peuvent pas changer le choix optimal. L'IA joue donc de façon optimale et ne perd pas contre un joueur qui joue lui aussi parfaitement.

## Installation et lancement

```bash
git clone https://github.com/cestbryan-ng/Minimax.git
cd Minimax
python -m pip install -r requirements.txt
python runner.py
```

Le projet utilise Pygame. La police `OpenSans-Regular.ttf` doit rester à côté de `runner.py`, car l'interface la charge depuis ce dossier.
