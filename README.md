import zipfile

# Contenu du README.md
readme_content = """# Msplomberie

Site web vitrine pour Msplomberie, entreprise de plomberie et chauffage à Nancy.

## Pages
- `index.html` : Accueil
- `services.html` : Nos services
- `contact.html` : Contact
- `localisation.html` : Localisation

## Style
Le site utilise un fichier CSS global `styles.css`.

## Déploiement sur GitHub Pages
Pour déployer le site sur GitHub Pages :

1. Crée un nouveau dépôt sur GitHub.
2. Uploade tous les fichiers du dossier msplomberie_site dans le dépôt.
3. Dans les paramètres du dépôt, active GitHub Pages.
4. Le site sera disponible à :
   `https://<votre-nom-utilisateur>.github.io/<nom-du-repo>/`
"""

# Nom du fichier et du ZIP
readme_file = "README.md"
zip_file = "README.zip"

# Écrire le README.md
with open(readme_file, "w", encoding="utf-8") as f:
    f.write(readme_content)

# Créer le ZIP
with zipfile.ZipFile(zip_file, "w") as zipf:
    zipf.write(readme_file)

print(f"Fichier ZIP créé : {zip_file}")