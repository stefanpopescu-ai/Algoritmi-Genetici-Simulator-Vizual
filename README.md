# 🧬 Algoritmi Genetici — Simulator Vizual

Un instrument educațional interactiv pentru vizualizarea pas cu pas a operațiilor unui algoritm genetic clasic. Aplicația rulează complet în browser, fără dependențe externe sau server.

---

## ✨ Funcționalități

### 1 — Populație
- Generează automat **16 cromozomi binari** de câte **12 gene** fiecare
- Valorile de fitness (10–100) sunt editabile direct în interfață
- Buton de regenerare completă a populației

### 2 — Selecție (Roata Ruletei)
- Calculează probabilitățile de selecție proporțional cu fitness-ul: `P(i) = f(i) / Σf`
- Vizualizează distribuția printr-o **roată a ruletei** colorată interactiv
- Extragere **pas cu pas** sau automată a celor 16 cromozomi pentru noua generație
- Tabel cu intervalele de selecție și bara de probabilitate pentru fiecare individ

### 3 — Încrucișare (Crossover Monocromatică)
- Fiecare cromozom selectat primește o valoare aleatorie `r`; dacă `r < p_c`, intră în lotul de încrucișare
- Vizualizare **pas cu pas** a schimbului de gene cu punct de tăiere aleatoriu
- **Caz special:** dacă lotul este impar și ≥ 3, ultimii trei participă la **încrucișare circulară**
- Descendenții înlocuiesc explicit părinții, cu un panou dedicat vizualizării înlocuirii

### 4 — Mutație (Inversare de Bit)
- Fiecare cromozom (post-încrucișare) primește o valoare aleatorie `r`; dacă `r ≤ p_m`, este mutat
- Alegere aleatorie a poziției și inversare a bitului, vizualizate **pas cu pas**
- Animație de evidențiere a genei afectate
- **Pasul 3** — comparație față în față între populația intrată în mutație și cea ieșită, cu biții modificați evidențiați în **violet** și statistici (cromozomi mutați, biți inversați)

### 5 — Rezultate
- Comparație **față în față** între generația 0 (originală) și generația 1 (finală)
- Genele modificate sunt evidențiate în roșu
- Statistici: cromozomi modificați, biți schimbați, contribuția încrucișării vs. mutației

---

## 🚀 Utilizare

Nu este necesară nicio instalare. Deschideți fișierul `algoritmi-genetici.html` direct în orice browser modern (Chrome, Firefox, Edge, Safari).

```
algoritmi-genetici.html   ← deschideți acest fișier
```

Parcurgeți taburile în ordine: **Populație → Selecție → Încrucișare → Mutație → Rezultate**.

---

## 🛠️ Tehnologii utilizate

| Tehnologie | Rol |
|---|---|
| HTML5 / CSS3 | Structură și stilizare |
| JavaScript (Vanilla) | Logica algoritmului și interactivitate |
| Canvas API | Desenarea roții ruletei |
| Google Fonts | Tipografie (JetBrains Mono, Syne) |

Aplicația este un **fișier HTML unic**, fără framework-uri, fără backend, fără dependențe npm.

---

## 📐 Parametri configurabili

| Parametru | Valoare implicită | Descriere |
|---|---|---|
| Număr cromozomi | 16 | Fix |
| Lungime cromozom | 12 gene | Fix |
| Fitness | 10–100 | Editabil per individ |
| Probabilitate încrucișare `p_c` | 0.25 | Editabil |
| Probabilitate mutație `p_m` | 0.20 | Editabil |

---

## 👤 Autor

Creat de **Ștefan Popescu** ca instrument educațional pentru studiul algoritmilor genetici.

Aplicația a fost dezvoltată cu ajutorul **Claude** (Anthropic) ca asistent AI — de la arhitectura inițială a interfeței, la implementarea logicii genetice pas cu pas, traducerea în limba română și designul temei luminoase.

---

## 📄 Licență

Proiect educațional cu uz liber. Redistribuirea cu menționarea autorului este încurajată.
