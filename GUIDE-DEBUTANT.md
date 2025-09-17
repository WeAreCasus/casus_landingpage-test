# 🎯 GUIDE DÉBUTANT - Comment modifier votre site Casus

Ce guide vous explique comment modifier facilement les éléments principaux de votre site web, même si vous êtes débutant en programmation !

## 📁 Structure des fichiers

Votre site a 3 versions qui s'adaptent automatiquement :
- `src/components/desktop/DesktopApp.tsx` - Version ordinateur
- `src/components/tablet/TabletApp.tsx` - Version tablette  
- `src/components/mobile/MobileApp.tsx` - Version mobile

**⚠️ IMPORTANT : Vous devez modifier les 3 fichiers pour que les changements apparaissent sur tous les appareils !**

## 🎨 Modifications les plus courantes

### 1. 🎯 CHANGER LE TITRE PRINCIPAL

**Où le trouver :** Cherchez ce commentaire dans les 3 fichiers :
```
🎯 TITRE PRINCIPAL - FACILE À MODIFIER
```

**Comment modifier :**
```jsx
<h1 className="text-5xl md:text-6xl lg:text-7xl font-bold text-white mb-8 leading-tight">
  L'IA fiscale qui libère{' '}
  <span className="bg-gradient-to-r from-purple-400 to-blue-400 bg-clip-text text-transparent">
    60% de votre temps
  </span>{' '}
  de recherche.
</h1>
```

- Modifiez le texte entre `<h1>` et `</h1>`
- Le texte dans `<span>` sera coloré en violet/bleu
- Gardez la même structure pour l'effet visuel

### 2. 📝 CHANGER LA DESCRIPTION

**Où le trouver :** Cherchez ce commentaire :
```
📝 DESCRIPTION PRINCIPALE - FACILE À MODIFIER
```

**Comment modifier :**
```jsx
<p className="text-xl md:text-2xl text-gray-300 mb-8 leading-relaxed">
  Facilitez vos recherches fiscales et obtenez des réponses expertes en quelques minutes. 
  La solution IA conçue spécifiquement pour les experts-comptables français.
</p>
```

- Modifiez le texte entre `<p>` et `</p>`
- Gardez 2 phrases pour un bon équilibre

### 3. 💰 CHANGER LES PRIX

#### Offre Starter
**Où le trouver :** Cherchez ce commentaire :
```
💰 OFFRE STARTER - FACILE À MODIFIER
```

**Comment modifier :**
```jsx
<h3 className="text-2xl font-bold text-white mb-1">Starter</h3>
<div className="text-gray-300 mb-4">Pour un usage modéré</div>
<div className="text-5xl font-bold text-white mb-1">€99</div>
```

- `Starter` = Nom de l'offre
- `Pour un usage modéré` = Description
- `€99` = Prix

#### Offre Pro (Recommandée)
**Où le trouver :** Cherchez ce commentaire :
```
🔥 OFFRE PRO (RECOMMANDÉE) - FACILE À MODIFIER
```

**Comment modifier :**
```jsx
<h3 className="text-2xl font-bold text-white mb-1">Pro</h3>
<div className="text-gray-300 mb-4">Pour les utilisateurs réguliers</div>
<div className="text-5xl font-bold text-white mr-3 line-through opacity-80">€149</div>
<div className="text-green-400 font-semibold">1 mois offert</div>
```

- `Pro` = Nom de l'offre
- `Pour les utilisateurs réguliers` = Description
- `€149` = Prix barré
- `1 mois offert` = Promotion

### 4. 📞 CHANGER LES INFORMATIONS DE CONTACT

**Où le trouver :** Cherchez ce commentaire :
```
📞 INFORMATIONS DE CONTACT - FACILE À MODIFIER
```

**Comment modifier :**
```jsx
<a href="https://www.linkedin.com/company/wearecasus/">LinkedIn</a>
<a href="mailto:contact@wearecasus.co">contact@wearecasus.co</a>
<a href="tel:0771670421">07 71 67 04 21</a>
```

- Modifiez le lien LinkedIn
- Modifiez l'email (dans `mailto:` et dans le texte)
- Modifiez le téléphone (dans `tel:` et dans le texte affiché)

### 5. ✨ CHANGER LES FONCTIONNALITÉS D'UNE OFFRE

**Comment modifier :**
```jsx
<li className="flex items-center text-gray-300">
  <CheckCircle2 className="w-5 h-5 text-green-400 mr-3" />
  30 recherches fiscales / mois
</li>
```

- Modifiez le texte après `mr-3" />`
- Gardez la structure avec `CheckCircle2` pour la coche verte

## 🖼️ Changer les photos des témoignages

Les photos se trouvent dans le dossier `public/` :
- `public/Kadi-seydi-photo.png`
- `public/charly-Goutorbe-photo.png`
- `public/leilla-Lecusson-photo.png`

**Pour changer une photo :**
1. Remplacez le fichier dans `public/` en gardant le même nom
2. Ou changez le nom dans le code :
```jsx
photo: "/nouveau-nom-photo.jpg"
```

## 🎨 Changer les couleurs

Les couleurs principales sont :
- Violet : `purple-500`, `purple-400`
- Bleu : `blue-500`, `blue-400`
- Vert : `green-400` (pour les coches)

**Exemple :**
```jsx
className="bg-purple-500"  // Fond violet
className="text-purple-400"  // Texte violet
```

## 🚀 Déployer vos modifications

Après avoir modifié les fichiers :

1. **Sauvegarder** vos changements
2. **Commit** avec Git :
```bash
git add .
git commit -m "Modification des prix et textes"
git push
```
3. **Vercel** déploiera automatiquement vos changements

## ⚠️ Conseils importants

1. **Testez toujours** sur les 3 appareils (desktop/tablet/mobile)
2. **Modifiez les 3 fichiers** pour la cohérence
3. **Gardez la structure** des balises HTML
4. **Faites des sauvegardes** avant de modifier
5. **Un changement à la fois** pour éviter les erreurs

## 🆘 En cas de problème

Si quelque chose ne marche plus :
1. Vérifiez que vous avez modifié les 3 fichiers
2. Vérifiez que vous n'avez pas supprimé de balises `<>` ou `</>`
3. Restaurez la version précédente avec Git
4. Contactez un développeur si nécessaire

---

**🎉 Félicitations ! Vous pouvez maintenant personnaliser votre site facilement !**
