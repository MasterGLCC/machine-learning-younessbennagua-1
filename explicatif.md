* Explicatif du travail

1) chargement du dataset
- Le fichier auto_mpg.csv contient des données sur des voitures (poids, chevaux, cylindres, année, consommation (MPG ou mile per galon))
- `le but est predire MPG à partir des autres variables`
- chargement du fichier csv en utilisant pandas 
- affichage de quelques informations a savoir ;
  les 5 premieres lignes (`head()`)
  statistiques:moyenne medianne...(`describe()`)
  valeurs manquantes (`isnull().sum()`)

2) regression from scratch
- simple:on predit MPG a partir du weight en calculant ŷ = b1·x + b0 avec la formules des moindres carres
- multiple:on predit MPG a partir de 4 var, avec les equqtions normale `β = (XᵀX)⁻¹ Xᵀy` on resout le systeme
- polynomiale: on predit MPG avec weight et weight², on fait une matrice comme suivant [1, x, x²] et on applique les equations normale precedente

2) regression avec scikit-learm
- simple:on predit MPG avec weight,`LinearRegression() cree le modele, fit() l'entraîne et calcule automatiquement b0 et b1 et predict() prédit les valeurs`
- multiple:on predit MPG a partir de 4 var, meme concept que la regression simple sauf que la bibliotheque scikit-learn calcule les coefficients β0,β1,β2.. automatiquemet depuis les equations normal
- polynomiale:on predit MPG avec weight et weight²,`PolynomialFeatures génère la matrice [1, x, x²], puis LinearRegression applique la régression dessus` et pipeline enchaine les 2 etapes



# R² : qualité du modèle
# MSE : erreur moyenne

NB: chaque version de regression  (from scratch/avec scikit-learn) contient une partie pour graphe qui genere 3 graphes (sipmle,multiple,polynomiale)