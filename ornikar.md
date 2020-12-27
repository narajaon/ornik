# SIGNALISATIONS

enum PanneauForme {
  rond = 'ordre'
  triangle = 'danger'
  carre = 'indication'
  fleche = 'direction'
  rectangle = 'localisation'
}

enum PanneauCarreCouleur {
  bleu = 'conseil'
}

enum PanneauTriangleCouleur {
  rouge = 'danger'
  jaune = 'temporaire'
}

enum PanneauRondCouleur {
  rouge = 'interdiction'
  bleu = 'obligation'
  jaune = 'temporaire'
}

interface Panonceau {
  avecFleche = boolean
}

interface Panneau {
  forme = PanneauForme
  estRempli = boolean
  panonceau = Panonceau
  couleur = PanneauCouleur
}

class PanneauDanger {
  form = 'triangle'
  couleur = estTemporaire ? 'jaune' : 'rouge'
  positionnement = enAgglomeration ? 50 : 150
  contenu = 'exclamation' | 'animal' | 'eboulement' | 'ravin' | 'chaussee retrecie'
}
