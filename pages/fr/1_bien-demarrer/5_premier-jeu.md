# Votre premier jeu

<div class="action">
  <p>**Créez une ressource de type Sprite**, appelez-le `Leonard`, ouvrez-le en double-cliquant dessus et uploadez une petite image.  
</div>

Assurez-vous de bien définir la taille de la grille, pour que l'image soit entiérement visible dans le panneau de prévisualisation (en bas).

<div class="action">
  <p>**Créez un script TypeScript**, appelez-le `Game` et ouvrez-le.
</div>

Les scripts sont utilisés pour indiquer à Superpowers que faire avec vos ressources. Quand vous lancez votre jeu, **Superpowers lit chaque script dans l'ordre, de haut en bas** et exécute les instructions situées à l'intérieur. Superpowers utilise <a href="http://www.typescriptlang.org/" target="_blank">TypeScript</a> comme language de script.

Métaphoriquement, votre jeu est comme un film dont vous êtes le metteur en scène. Dans vos scripts, vous indiquez quels acteurs participent, quels costumes ils doivent enfiler et quels seront leurs rôles. Sans script, tout le monde restera dans les coulisses, personne ne sera sur le plateau et l'écran restera donc noir.

<div class="action">
  <p>Dans l'éditeur de script, supprimez le texte de base et tapez le code suivant (ou copier / coller, mais vous apprendrez plus vite si vous tapez tout vous même) :
</div>

```
// Appelons notre premier acteur sur le plateau, il jouera le personnage principal
let mainCharacterActor = new Sup.Actor("Main Character");
// Disons à notre acteur de mettre le costume (sprite) "Leonard"
new Sup.SpriteRenderer(mainCharacterActor, Sup.get("Leonard", Sup.Sprite));

// Appelons une seconde personne sur le plateau, ce sera notre caméraman
let cameraManActor = new Sup.Actor("Camera Man");
// Donnons lui une caméra
new Sup.Camera(cameraManActor);

// Plaçons nos acteurs. Le personnage principal est au centre de la scène
mainCharacterActor.setPosition(new Sup.Math.Vector3(0,0,0));

// Le caméraman doit s'éloigner pour filmer l'acteur principal
cameraManActor.setPosition(new Sup.Math.Vector3(0,0,5));
```

<p>Les lignes commençant par `//` sont des commentaires. Superpowers ne fait pas attention à ces lignes, elles ne sont là que pour expliquer comment tout fonctionne.</p>

<div class="note">
  <p><b>IMPORTANT:</b> Appuyez sur `Ctrl+S` pour appliquer les changements faits dans vos scripts. Vous remarquez que l'indicateur `draft` dans l'arbre de ressources disparaît quand votre script est sauvegardé.</p>
</div>

Superpowers peut détecter certaines erreurs de script (erreurs de syntaxe, référence ou de type) à la volée, donc si vous voyez des mots en rouges quand vous avez fini, vous savez que vous devez relire ces lignes et les lignes autour. Les messages d'erreurs détaillés sont affichés en bas de l'éditeur.

Quand vous avez fini, lancez votre jeu avec le bouton `Run game` et vous devriez voir votre acteur apparaître !