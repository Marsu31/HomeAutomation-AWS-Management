# HomeAutomation-AWS-Management
Home automation management with AWS services (IoT, Lambdas)

## Besoin

* **actionner la domotique depuis internet**. L'utilisation d'AWS permet de créer émetteur MQTT dont on maîtrise les adresses IP pour le filtrage au niveau du firwall.
 * **compatible Android**. En installant un client MQTT sur le téléphone. Le service AWS se comporte alors comme un proxy.
 * **compatible navigateur**. Une appli web se charge de recueillir la saisie de l'utilisateur.
* **protéger le LAN**. Ne pas exposer le réseau local sur Internet.
* **protéger la maison**. Les accès doivent être extrêmement sécurisés.

## Attention

* **A la tarification AWS**
 * Au bout de 1 an, l'utilisation des services IoT et S3 deviennent payants sans seuil de gratuité (contrairement aux Lambdas).
 * Les régions facturent différemment. La côte est des US est la moins chère.

* **A la disponibilté des services**. A l'heure de la rédaction de ce paragraphe le service IoT est absent du territoire français.

## Spécifications techniques

### Développement

* **IoT**. Réflexion à mener sur la syntaxe des topics.
* **Appli Web**. Les technologies utilisée seront Angular déployé sur S3, Api Gateway (Api REST), Lambdas en Node ou Python (choix encore indécis).
* **Cloudwatch**. Pour l'application web.
* **CLI AWS**. Pour l'IoT.
* **Workflow de déploiement** ?
* **Swagger** ?

### Sécurité

* **IoT**. Le service est déjà sécurié grace à de solides certificats.
* **Appli Web**
 * Droits sur le bucket S3. https://aws.amazon.com/fr/blogs/security/how-to-use-bucket-policies-and-apply-defense-in-depth-to-help-secure-your-amazon-s3-data/
 * Droits sur l'Api Gateway.
   * https://aws.amazon.com/fr/blogs/compute/protecting-your-api-using-amazon-api-gateway-and-aws-waf-part-i/
   * https://aws.amazon.com/fr/blogs/compute/protecting-your-api-using-amazon-api-gateway-and-aws-waf-part-2/?nc1=b_rp
   * https://aws.amazon.com/fr/waf/
 * Droits sur les Lambdas.

## Références

*déplacer ici les liens une fois lus*
