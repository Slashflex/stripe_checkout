## Application basique de paiement en ligne avec Stripe

#### Installation
Une fois le dépôt clôné, placez vous dans ce dossier, puis installez les dépendences requises:
```sh
npm install
```

Veillez a changer les clés d'API STRIPE:
dans le fichier ```app.js``` ligne 1:
```js
const stripe = Stripe('VOTRE CLE PUBLIQUE STRIPE');
```
et dans le fichier ```server.js``` ligne 4
```js
const stripe = require('stripe')('VOTRE CLE SECRETE STRIPE');
```

Pour lancer le server NodeJS:
```sh
npm run start
# ou 
npm start
```

Il ne reste plus qu'à tester. Stripe fournit des numéros de carte de test

|       Numéro        |           Description           |
| :-----------------: | :-----------------------------: |
| 4242 4242 4242 4242 |  Paiement validé immédiatement  |
| 4000 0025 0000 3155 |        Active 3D Secure         |
| 4000 0000 0000 9995 | Echoue sur "Fonds insuffisants" |

La date d'expiration doit être supérieure à la date à laquelle vous souhaitez effectuer le paiement.

Le code de vérification CVC peut être n'importe quel nombre à 3 trois chiffres (ex: 123)# stripe_checkout
