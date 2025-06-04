## 📍 Étape 1 : Rencontre chef de mission

### 🔸 Respect des échéances (Respect des délais)

**Formule** :

$$
\text{Score} = \max\left(0, \min\left[\left(1 - \frac{|\text{Temps référence} - \text{Temps utilisateur}|}{\text{Temps référence}} - \frac{\text{Pénalités} \times \text{Pénalité par unité}}{\text{Temps référence}}\right) \times 100, 100\right]\right)
$$

**Explication** :
Cette formule mesure la capacité à respecter un temps imparti, en prenant en compte deux facteurs :

* L’écart absolu entre le temps prévu et le temps réel (normalisé).
* Les pénalités converties en secondes.

Le score est ramené à une échelle de 0 à 100, avec protection contre les valeurs négatives ou excessives.

---

### 🔸 Score de mémorisation

**Formule** :

$$
\text{Score} = \left(\frac{\text{Nombre de bonnes réponses}}{3}\right) \times 100
$$

**Explication** :
Évalue la mémoire à court terme à travers un quiz de 3 questions. Le score est proportionnel au nombre de bonnes réponses.

---

### 🔸 Temps mis

**Formule** :

$$
\text{Score} = \text{Temps utilisateur (en secondes)}
$$

**Explication** :
Valeur brute du temps passé à réaliser cette étape. Utilisée à des fins analytiques, non comme une note.

---

## 📍 Étape 2 : Analyse des indicateurs des agences

### 🔸 Précision documentaire

**Formule** :

$$
\text{Score} = \max\left(0, \min\left[\left(\frac{5}{\text{Documents ouverts}} \times 50 + \frac{1}{\text{Nombre d’essais}} \times 50\right) \times \text{Participation}, 100\right]\right)
$$

**Explication** :
Mesure l’efficacité documentaire :

* Moins de documents ouverts → meilleur score.
* Moins d’essais → meilleur score.
  Le tout est conditionné à la participation effective de l’utilisateur à l’étape.

---

### 🔸 Temps mis

**Formule** :

$$
\text{Score} = \text{Temps utilisateur (en secondes)}
$$

**Explication** :
Temps brut passé sur l’étape, à des fins de traçabilité ou d’analyse.

---

## 📍 Étape 3 : Mapping des agences moins scorées

### 🔸 Précision documentaire

**Formule** :

$$
\text{Score} = \max\left(0, \min\left[\left(\frac{5}{\text{Documents ouverts}} \times 50 + \frac{1}{\max(\text{Essais}, 1)} \times 50\right) \times \text{Participation}, 100\right]\right)
$$

**Explication** :
Formule identique à celle de l’étape 2, avec un ajustement pour éviter la division par zéro.

---

### 🔸 Temps mis

**Formule** :

$$
\text{Score} = \text{Temps utilisateur (en secondes)}
$$

---

## 📍 Étape 4 : Planification des missions

### 🔸 Priorisation

**Formule** :

$$
\text{Score} = \left[\max\left(0, \min\left(100 - \left(\min\left(30, \frac{\text{Drag\&Drop} - \text{Drag\&Drop optimal}}{\text{Drag\&Drop optimal}} \times 30\right) + \min\left(20, \frac{\text{Validations} - \text{Validations optimales}}{\text{Validations optimales}} \times 20\right)\right), 100\right)\right)\right] \times \text{Participation}
$$

**Explication** :
Penalise l’excès d’interactions. Plus les actions dépassent les seuils optimaux, plus le score diminue.

---

### 🔸 Temps mis

**Formule** :

$$
\text{Score} = \text{Temps utilisateur (en secondes)}
$$

---

## 📍 Étape 5 : Lancement de la mission

### 🔸 Réactivité stratégique

**Formule** :

$$
\text{Score} = \text{Participation} \times \left(\frac{1}{1 + \text{Erreurs}}\right) \times \left(\frac{1}{1 + \frac{\text{Temps de réflexion}}{30}}\right)
$$

**Explication** :
Évalue la rapidité et la précision de la réaction. Score compris entre 0 et 1 :

* Moins d’erreurs → meilleur score.
* Réflexion rapide → meilleur score.

---

### 🔸 Temps mis

**Formule** :

$$
\text{Score} = \text{Temps utilisateur (en secondes)}
$$

---

## 📍 Étape 6 : Audit des comptes

### 🔸 Séquencement logique

**Formule** :

$$
\text{Score} = \left(\frac{\text{Positions correctes}}{4}\right) \times 100
$$

---

### 🔸 Précision analytique

**Formule** :

$$
\text{Score} = \left( \frac{2PR}{P + R} \times 0.5 + \text{Score Commentaires} \times 0.5 \right) \times \text{Participation}
$$

où :

* $P = \frac{\text{Anomalies correctes}}{\text{Documents sélectionnés}}$
* $R = \frac{\text{Anomalies correctes}}{\text{Total anomalies}}$
* Score commentaires = moyenne de 4 notes

---

### 🔸 Détection d’erreurs

**Formule** :

$$
\text{Score} = \left( \frac{2PR}{P + R} \times 0.5 \right) \times \text{Participation}
$$

---

### 🔸 Temps mis

**Formule** :

$$
\text{Score} = \text{Temps utilisateur (en secondes)}
$$

---

## 📍 Étape 7 : Dossier sécurisé

### 🔸 Efficacité de résolution

**Formule** :

$$
\text{Score} = \max\left(0, 100 - \left[\text{Fibonacci}(\text{Essais}) - \frac{\text{Essais}}{54}\right] \times 100\right)
$$

**Explication** :
Une croissance exponentielle pénalise l’abus d’essais.

---

### 🔸 Temps mis

**Formule** :

$$
\text{Score} = \text{Temps utilisateur (en secondes)}
$$

---

## 📍 Étape 8 : Responsabilité des anomalies

### 🔸 Détection de patterns

**Formule** :

$$
\text{Score} = \max\left(0, \left(\frac{\text{Réponses correctes}}{7} - \frac{\text{Réponses incorrectes}}{50}\right) \times 100\right)
$$

---

### 🔸 Temps mis

**Formule** :

$$
\text{Score} = \text{Temps utilisateur (en secondes)}
$$

---

## 📍 Étape 9 : Emails frauduleux

### 🔸 Identification des menaces

**Formule** :

$$
\text{Score} = \text{Score booléen} \times 100
$$

---

### 🔸 Qualité décisionnelle

**Formule** :

$$
\text{Score} = \text{Score booléen} \times 100
$$

---

### 🔸 Temps mis

**Formule** :

$$
\text{Score} = \text{Temps utilisateur (en secondes)}
$$

---

## 📍 Étape 10 : Interrogatoire en réunion

### 🔸 Choix de dialogue / Gestion des conflits / Persuasion / Pression

**Formule (pour chaque)** :

$$
\text{Score} = \text{Valeur brute fournie}
$$

---

### 🔸 Temps mis

**Formule** :

$$
\text{Score} = \text{Temps utilisateur (en secondes)}
$$

---

## 📍 Étape 11 : Hard Skills

### 🔸 Question 1 – ROE

**Formule** :

$$
\text{Score} = b(\text{ROE 2021} = 22.86) \times b(\text{ROE 2024} = 45.71) \times 100
$$

---

### 🔸 Question 2 – ROA

**Formule** :

$$
\text{Score} = b(\text{ROA 2021} = 13.33) \times b(\text{ROA 2024} = 21.33) \times 100
$$

---

### 🔸 Question 3 – Ratio de liquidité

**Formule** :

$$
\text{Score} = b(\text{Ratio 2024} = 1.67) \times 100
$$

---

### 🔸 Question 4 – TCAM

**Formule** :

$$
\text{Score} = b(\text{TCAM} = 14.47) \times 100
$$

---

### 🔸 Synthèse et Avis

**Formule** :

$$
\text{Score} = \text{Score donné par l'IA}
$$
