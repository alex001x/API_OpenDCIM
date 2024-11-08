# API_OpenDCIM
Ici, je poste les codes vb API OpenDCIM utilisés pour LibreOffice Calc et Ms Excel que je mets à disposition aux fur et à mesure de l'avancement, c'est quelque chose que je fais en dehors de mon travail.

API_PduStat
Code permettant l'envoie à OpenDCIM des saisies des metrics pdu ( pour ceux qui ne souhaite pas les connecter/administrer) depuis un tableau excel ou calc LibreOffice.
Vous pouvez aussi créer un script (construction de la syntaxe snmpget) qui recolte les données des PDU, avec un appel API pour récupérer la liste des IP des PDU à consulter et les paramétrages SNMP, puis un envoi API pour transmettre les données à OpenDCIM.
Solution alternative selon les différents niveaux de sécurité.

API Pdustat Excel -> Feuille Excel -En cours d'édition
![image](https://github.com/user-attachments/assets/cc458c17-3515-464e-8f2e-bbef70c4b88a)

API Pdustat Calc -> Feuille calc Libre office
![image](https://github.com/user-attachments/assets/24b0dd4e-eac8-439e-ab7b-afa6df1a3e4e)

Les 3 premières colonnes ABC sont nécessaires pour la construction de la syntaxe curl, "pduid, wattage et date", les autes colonnes à partir de la colonne D existe pour facilité la lecteure du fichier par les tech ou équipe de proximité
image, La liste des PDU et les informations DevicesID sont récupérés deppuis DCIM avec la finction API_GET_PDUStat, vous ppouvez filtré les PDU qui ont la case "Manage" cochée, ou autre type de critère.
Mode formulaire, création d'un bouton, editer une macro et ajouter la macro à votre feuille quitter le mode création formulaire
Saisir un identifiant correspondant à votre PDU (export des données possible depuis la section rapport inventaire)
Les cellules ABC ne peuvent être vide ou érroné
