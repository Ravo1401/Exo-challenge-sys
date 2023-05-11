# FTP-Authentification
- Donc il faut commencer par démarrer le challenge (Téléchargement d'un fichier nommée ch1.pcap)
- Ouvrir le fichier télécharger sur Wireshark
- Clic droit sur un protocole FTP
- Suivre son flux TCP Stream
- Le mot de passe est à côté de PASS: cd******
- Puis entrer le mot de passe dans le challenge

# TELNET-Authentification
- Comme d'habitude démarrer le challenge (Téléchargement d'un fichier nommée ch2.pcap)
- Ouvrir le fichier avec Wireshark
- Clic droit sur un des protocoles TCP et suivre son flux TCP Stream
- Le mot de passe se trouve à côté de password : u***

# ETHERNET-trame
- Démarrer le challenge 
- Après il vous dirige vers un nouvelle onglet plein de hexadécimal
- Il faut les convertir dans le site "Convert hexadecimal to text" et on a le mot de passe à côté de Authorization: Basic (Y****************) mais il est en base64 
- Décoder le mot de passe à l'aide d'un site "Base64 decode and encode" puis on a le dernier mot de passe : c***********

# Authentification twitter
- Démarrer le challenge (Téléchargement d'un fichier nommée ch3.pcap)
- Ouvrir le fichier avec Wireshark
- Clic droit sur le protocole HTTP et suivre son flux TCP Stream
- Le mot de passe est à côté de Authorization: Basic d**********************
- Décoder le mot de passe à l'aide d'un site "Base64 decode and encode" puis on a le dernier mot de passe du challenge est : p*******

# Bluetooth-Fichier inconnu
- Démarrer le challenge (Téléchargement d'un fichier nommée ch18.pcap)
- Ouvrir le fichier avec Wireshark
- Aller dans la barre d'outil: Wireless> Bluetooth devices, puis le nom du téléphone et son adresse MAC s'affiche: 0c:b3:19:b9:4f:c6 SamsungE GT-S7390G
- Il faut changer les lettres minuscules en majuscules: 0C:B3:19:B9:4F:C6GT-S7390G
- Encrypter cette concaténation à l'aide du site SHA1: "Crypter avec sha1 en ligne" puis on obtient le mot de passe final : c1**************************************