# Ajout du son au mini-jeu Super Nathan Run

**Date:** 2026-03-28 12:30
**Statut:** Terminé

## Contexte
Le mini-jeu game.html n'avait aucun son. On ajoute la bande son Mario (même musique que l'index), un son de saut "bip-biiiip" ascendant, et le son de mort Mario quand on meurt.

## Modifications
- [x] `game.html` - Ajout système audio complet (Web Audio API)
  - Musique de fond SMB1 Overworld (identique à index.html)
  - Son de saut : double beep ascendant (square wave 500→800Hz puis 700→1200Hz)
  - Son de mort Mario : séquence de notes descendantes (B4 A4 D4 F4 G4 D4 E4 C4)
  - La musique démarre au premier saut, s'arrête à la mort, reprend au replay
  - Unlock iOS AudioContext au premier tap

## Notes
- Audio initialisé au premier input utilisateur pour compatibilité iOS Safari
- La musique est stoppée à la mort pour laisser entendre le son de mort
- Elle redémarre quand le joueur relance une partie

## Rollback
Reverter le fichier game.html au commit précédent : `git checkout HEAD -- game.html`
