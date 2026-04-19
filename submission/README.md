# TP — Exploration de Gymnasium (Taxi-v3 & MiniGrid-Empty-16x16-v0)

**Module :** M2442 — Introduction à Gymnasium (Pr. Youness BOUTYOUR)
**Auteur :** Moubarak Benaqqa — ENSIAS
**Date :** avril 2026

## Contenu

- `TP_Gymnasium_Taxi_MiniGrid_Etudiant_v2.ipynb` — notebook complété et **déjà exécuté** (résultats et figures intégrés).
- `videos/` — enregistrements vidéo des politiques (MiniGrid aléatoire, MiniGrid mémoire, Taxi heuristique).
- `requirements.txt` — dépendances Python pour réexécuter le notebook.

## Installation

```bash
pip install -r requirements.txt
```

## Réexécution

```bash
jupyter nbconvert --to notebook --execute TP_Gymnasium_Taxi_MiniGrid_Etudiant_v2.ipynb \
    --output TP_Gymnasium_Taxi_MiniGrid_Etudiant_v2.ipynb
```

## Résumé des résultats obtenus

| Environnement | Politique | Récompense moyenne | Étapes moyennes | Taux de succès |
|---|---:|---:|---:|---:|
| Taxi-v3 | Aléatoire | ≈ −754 | 200 | 0 % |
| Taxi-v3 | Aléatoire contrainte (`action_mask`) | ≈ −186 | ≈ 190 | 17.5 % |
| Taxi-v3 | Heuristique (BFS + pickup/dropoff) | **+7.5** | **13.5** | **100 %** |
| MiniGrid-Empty-16x16 | Aléatoire | ≈ 0.04 | ≈ 999 | 15 % |
| MiniGrid-Empty-16x16 | Réflexe (avancer / sinon droite) | **+0.98** | **27** | **100 %** |
| MiniGrid-Empty-16x16 | Mémoire minimale | **+0.98** | **27** | **100 %** |

## Structure du notebook

1. Installation et imports
2. Fonction utilitaire d'évaluation
3. **Partie A** — Découverte de Taxi-v3 (+ réponses)
4. **Partie B** — Politique aléatoire sur Taxi-v3 (+ réponses)
5. **Partie C** — Politique aléatoire contrainte sur Taxi-v3 (+ réponses)
6. **Partie D** — Politique heuristique (BFS) pour Taxi-v3 (+ réponses)
7. Tableau comparatif des trois politiques Taxi
8. **Partie E** — Découverte de MiniGrid-Empty-16x16-v0 (+ réponses)
9. **Partie F** — Politique aléatoire sur MiniGrid (+ réponses)
10. **Partie G** — Politique réflexe minimale sur MiniGrid (+ réponses)
11. **Partie H** — Politique d'exploration avec mémoire minimale (+ réponses)
12. Wrapper `RecordEpisodeStatistics`
13. **Partie I** — Comparaison finale et figure
14. Questions de synthèse
15. Extension — Visualisation par images et vidéos (+ analyse visuelle)

Toutes les questions de l'énoncé (`ennonce.pdf`) sont traitées dans les cellules Markdown du notebook.
