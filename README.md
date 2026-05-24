# Digital Theremin + SimpleOscillator
Digital theremin este un generator note MIDI pe baza pozitiei mouse-ului pe ecran
;
- Canal 1 - note obtinute din pozitia cusrorului pe axa orizontala
- Canal 2 - note obtinute din pozitia cursorului pe axa verticala
;
Features:
- Este sincronizat cu tempo-ul setat in DAW
- Nu este nevoie de mouse pentru a schimba setarile, lasand loc pentru miscarea libera a acestui in timpul utilizarii patch-ului.
;
Controls:
- ` = pornire/oprire
- Q, W, E, R, T, Y, A, S, D, F, G, H = alegere root note al gamei (C, C#... A#, B)
- Z, X, C, V, B, N = alegere mod al gamei (Ionian, Dorian, Phrygian, Lydian, Mixolydian, Aeolian)

SimpleOscillator este un patch de sintetizatoare compatibil cu orice track MIDI.

## (Instalare)
1. Instaleaza PlugData
2. Instaleaza pachetul VST PlugData
3. Instaleaza un DAW compatibil cu VST-ul PlugData
4. Descarca patch-ul oriunde

## (Utilizare)
1. Creeaza un proiect in DAW (eu am folosit Studio One 5)
2. Creeaza 3 track-uri
3. Adauga instrumentul PlugData si deschide patch-ul DigitalTheremin.pd
4. Configureaza primul track sa primeasca input de instrumentul PlugData recent adaugat
5. El isi configureaza automat outputurile pe MIDI 1 si MIDI 2
6. Celelalte doua track-uri pot contine orice instrument MIDI (pentru a asculta output-ul DigitalTheremin live, trebuie configurate)
7. Apasa ` pentru a porni DigitalTheremin
8. Apasa butonul "Record" pentru a inregistra track-uri MIDI cu mouse-ul!

## (Istoric)
(06.04)
- Ideea proiectului a inceput cu tema "Comms"
- Am creat o versiune a DigitalTheremin care norma la nota A (La) = 440Hz, prin operatiuni matematice si logice, coordonatele X si Y ale cursorului
- Problema era ca nu se putea conecta la DAW si nu scotea MIDI ca output
  
(25.04) 
Primul target al acestui proiect a fost sa-l fac functional si compatibil cu un DAW. Pana la finalizarea proiectului, voi adauga:
- Un patch cu sintetizatoare, care sa poata fi folosite drept output-uri in DAW
- Integrare deplina cu DAW-ul, prin intermediul parametrilor
- Mai multe controale din tastatura (spre exemplu, alegerea prin tastatura a gamei sau a modului)
- Un toggle pentru output-ul acordurilor + 3-4 tipuri de acorduri (sa zicem Maj/Min/7th/9th)
- O interfata grafica care poate ascunde firele din PD
- Voi exporta instrumentul ca un plugin VST

(30.04)
- Am adaugat un GUI rudimentar, mai multe keybind-uri pentru flexibilitate in timpul utilizarii instrumentului, si am rafinat oscilatorul.
- Implementare GUI
- Implementare compatibilitate cu tastatura
- Curatarea si eficientizarea logicii din cod pentru a elimina pauzele in DAW
- Salvarea parametrilor din patch pentru utilizarea in sesiuni separate
  
(24.05)
- Adaugare documentatie si creare fork
  
## (Link-uri)
- https://www.youtube.com/watch?v=PKZfqMb8buY&t=6s
- https://www.youtube.com/watch?v=QwC7P9LUXU8
- https://www.youtube.com/watch?v=hXKFPXkcqLk

# Dezvoltarea proiectului

Pentru început:

1. Creează-ți cont pe Github
2. Download și install [Github Desktop](https://desktop.github.com/)
3. Citește [acest ghid](https://charlesmartin.com.au/blog/2020/08/09/student-project-repository) și ține la îndemână [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet).

Apoi, procesul este următorul (inspirat de [aici](https://cs.anu.edu.au/courses/comp1720/deliverables/05-major-project/#submission-process)):

1. *fork* al acestui template către propriul tău cont de Github

![](assets/fork.gif)

_(dacă preferi cumva ca repo-ul să nu fie vizibil de către public, îl poți seta ca Private din Settings - "Change visibility". Atunci trebuie să mă adaugi drept colaborator, ca eu să am acces.)_

2. *clone* al repo-ului din Github Desktop pentru a-l downloada local

![](assets/clone.gif)

3. *commit* și *push* pe măsură ce lucrezi la proiect. Ultima versiune push-ată pe server înainte de deadline va conta pentru evaluare.

![](assets/commit.gif)

## Elemente obligatorii

1. Acest readme completat. Titlu, descriere, mod de utilizare, istoric, link-uri utile.

   Poți include și imagini și chiar [gif-uri animate](https://www.screentogif.com/), sau link-uri către materiale audio/video.
   
   Vezi [aici](https://charlesmartin.com.au/blog/2020/08/09/student-project-repository) mai multe sugestii.

2. [Declarația de originalitate](statement-of-originality.yml) completată. Tot ce nu este inclus acolo va fi considerat 100% contribuție proprie.

    *(formatul este adaptat de [aici](https://gitlab.cecs.anu.edu.au/comp1720/2018/comp1720-2018-major-project/-/blob/master/statement-of-originality.yml). Da, este un pic ironic să refolosim un doc [de altundeva](https://cs.anu.edu.au/courses/comp1720/resources/faq/#how-do-i-fill-out-my-statement-of-originality), dar menționăm sursa deci nu este plagiat!)*

3. Proiectul în sine. Tot codul trebuie să fie prezent, proiectul trebuie să poată rula conform instrucțiunilor din readme. Dacă e nevoie de asset-uri mari (sunete, video etc), [folosește Git LFS](https://git-lfs.github.com/) sau include link de download în instrucțiunile de instalare.

