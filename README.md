# mathematica
For[t = 1, t <= 16, t++,
 gradsquared =
  Table[piprimedata[[Floor[Mod[i - 1, 1/meshsize] + 1]]][[Floor[
        Mod[j - 1, 1/meshsize] + 1]]][[Floor[
       Mod[k - 1, 1/meshsize] + 1]]] +
    2/time pidata[[Floor[Mod[i - 1, 1/meshsize] + 1]]][[Floor[
         Mod[j - 1, 1/meshsize] + 1]]][[Floor[
        Mod[k - 1, 1/meshsize] + 1]]] +
    1/(8 meshsize^2) ((pidata[[
            Floor[Mod[i + 1 - 1, 1/meshsize] + 1]]][[
           Floor[Mod[j - 1, 1/meshsize] + 1]]][[
          Floor[Mod[k - 1, 1/meshsize] + 1]]] -
         pidata[[Floor[Mod[i - 1 - 1, 1/meshsize] + 1]]][[
           Floor[Mod[j - 1, 1/meshsize] + 1]]][[
          Floor[Mod[k - 1, 1/meshsize] + 1]]])^2 + (pidata[[
            Floor[Mod[i - 1, 1/meshsize] + 1]]][[
           Floor[Mod[j + 1 - 1, 1/meshsize] + 1]]][[
          Floor[Mod[k - 1, 1/meshsize] + 1]]] -
         pidata[[Floor[Mod[i - 1, 1/meshsize] + 1]]][[
           Floor[Mod[j - 1 - 1, 1/meshsize] + 1]]][[
          Floor[Mod[k - 1, 1/meshsize] + 1]]])^2 + (pidata[[
            Floor[Mod[i - 1, 1/meshsize] + 1]]][[
           Floor[Mod[j - 1, 1/meshsize] + 1]]][[
          Floor[Mod[k + 1 - 1, 1/meshsize] + 1]]] -
         pidata[[Floor[Mod[i - 1, 1/meshsize] + 1]]][[
           Floor[Mod[j - 1, 1/meshsize] + 1]]][[
          Floor[Mod[k - 1 - 1, 1/meshsize] + 1]]])^2), {i, 1, 1/
    meshsize}, {j, 1, 1/meshsize}, {k, 1, 1/meshsize}];
 sum = Sum[(-(6/
        time^2) (1/(
         4 meshsize^2) (pidata[[Floor[
                Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r - 1, 1/meshsize] + 1]]] +
           pidata[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r - 1, 1/meshsize] + 1]]] -
           2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
                Mod[q - 1, 1/meshsize] + 1]]][[Floor[
               Mod[r - 1, 1/meshsize] + 1]]] +
           pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r - 1, 1/meshsize] + 1]]] +
           pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r - 1, 1/meshsize] + 1]]] -
           2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
                Mod[q - 1, 1/meshsize] + 1]]][[Floor[
               Mod[r - 1, 1/meshsize] + 1]]] +
           pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r + 2 - 1, 1/meshsize] + 1]]] +
           pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r - 2 - 1, 1/meshsize] + 1]]] -
           2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
                Mod[q - 1, 1/meshsize] + 1]]][[Floor[
               Mod[r - 1, 1/meshsize] + 1]]])) +
      1/(4 meshsize^2) (pidata[[Floor[
              Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         pidata[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] +
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] -
         2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]]) 1/(
       4 meshsize^2) (gradsquared[[Floor[
              Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]]) +
      1/(2 meshsize) (pidata[[Floor[
              Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         pidata[[Floor[Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]]) 1/(
       8 meshsize^3) (gradsquared[[Floor[
              Mod[p + 3 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         3 gradsquared[[Floor[
               Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         3 gradsquared[[Floor[
               Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 3 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[
               Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[
               Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[
               Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[
               Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]]) +
      1/(2 meshsize) (pidata[[Floor[
              Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]]) 1/(
       8 meshsize^3) (gradsquared[[Floor[
              Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 3 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         3 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         3 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 3 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]]) +
      1/(2 meshsize) (pidata[[Floor[
              Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 1 - 1, 1/meshsize] + 1]]] -
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1 - 1, 1/meshsize] + 1]]]) 1/(
       8 meshsize^3) (gradsquared[[Floor[
              Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 3 - 1, 1/meshsize] + 1]]] -
         3 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r + 1 - 1, 1/meshsize] + 1]]] +
         3 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 3 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 1 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 1 - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r + 1 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1 - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 1 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 1 - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r + 1 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1 - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1 - 1, 1/meshsize] + 1]]])) meshsize^3, {p, 1, 1/
    meshsize}, {q, 1, 1/meshsize}, {r, 1, 1/meshsize}];
 integrand =
  Table[(-(6/
        time^2) (1/(
         4 meshsize^2) (pidata[[Floor[
                Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r - 1, 1/meshsize] + 1]]] +
           pidata[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r - 1, 1/meshsize] + 1]]] -
           2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
                Mod[q - 1, 1/meshsize] + 1]]][[Floor[
               Mod[r - 1, 1/meshsize] + 1]]] +
           pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r - 1, 1/meshsize] + 1]]] +
           pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r - 1, 1/meshsize] + 1]]] -
           2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
                Mod[q - 1, 1/meshsize] + 1]]][[Floor[
               Mod[r - 1, 1/meshsize] + 1]]] +
           pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r + 2 - 1, 1/meshsize] + 1]]] +
           pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
               Mod[q - 1, 1/meshsize] + 1]]][[Floor[
              Mod[r - 2 - 1, 1/meshsize] + 1]]] -
           2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
                Mod[q - 1, 1/meshsize] + 1]]][[Floor[
               Mod[r - 1, 1/meshsize] + 1]]])) +
      1/(4 meshsize^2) (pidata[[Floor[
              Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         pidata[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] +
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] -
         2 pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]]) 1/(
       4 meshsize^2) (gradsquared[[Floor[
              Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]]) +
      1/(2 meshsize) (pidata[[Floor[
              Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         pidata[[Floor[Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]]) 1/(
       8 meshsize^3) (gradsquared[[Floor[
              Mod[p + 3 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         3 gradsquared[[Floor[
               Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         3 gradsquared[[Floor[
               Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 3 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[
               Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[
               Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[
               Mod[p + 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[
               Mod[p - 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]]) +
      1/(2 meshsize) (pidata[[Floor[
              Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]]) 1/(
       8 meshsize^3) (gradsquared[[Floor[
              Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 3 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         3 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         3 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 3 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 2 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 2 - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1, 1/meshsize] + 1]]]) +
      1/(2 meshsize) (pidata[[Floor[
              Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 1 - 1, 1/meshsize] + 1]]] -
         pidata[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1 - 1, 1/meshsize] + 1]]]) 1/(
       8 meshsize^3) (gradsquared[[Floor[
              Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 3 - 1, 1/meshsize] + 1]]] -
         3 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r + 1 - 1, 1/meshsize] + 1]]] +
         3 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 3 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 1 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 1 - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r + 1 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q + 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 2 - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1 - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 1 - 1, 1/meshsize] + 1]]] +
         gradsquared[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r + 1 - 1, 1/meshsize] + 1]]] -
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r + 1 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p + 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1 - 1, 1/meshsize] + 1]]] -
         gradsquared[[Floor[Mod[p - 2 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[q - 1, 1/meshsize] + 1]]][[Floor[
            Mod[r - 1 - 1, 1/meshsize] + 1]]] +
         2 gradsquared[[Floor[Mod[p - 1, 1/meshsize] + 1]]][[Floor[
              Mod[q - 1, 1/meshsize] + 1]]][[Floor[
             Mod[r - 1 - 1, 1/meshsize] + 1]]])) - sum*meshsize^3, {p,
     1, 1/meshsize}, {q, 1, 1/meshsize}, {r, 1, 1/meshsize}];
 FT = Fourier[integrand];
 FTinverseLaplacian =
  Table[Table[
    Table[((-1)/(4 Pi^2 ((Min[(i - 1),
              1/meshsize - (i - 1)])^2 + (Min[(j - 1),
              1/meshsize - (j - 1)])^2 + (Min[(k - 1),
              1/meshsize - (k - 1)])^2 +
            0.001^2))) FT[[i]][[j]][[k]], {k, 1,
      Length[FT[[i]][[j]]]}], {j, 1, Length[FT[[i]]]}], {i, 1,
    Length[FT]}];
 InverseLaplacian = InverseFourier[FTinverseLaplacian];
 integral =
  Table[Re[InverseLaplacian[[i]][[j]][[k]]], {i, 1, 1/meshsize}, {j,
    1, 1/meshsize}, {k, 1, 1/meshsize}];
 pidatanext =
  Table[(pidata[[i]][[j]][[k]]) + (piprimedata[[i]][[j]][[k]])*
     timestep, {i, 1, 1/meshsize}, {j, 1, 1/meshsize}, {k, 1, 1/
    meshsize}];
 piprimedatanext =
  Table[piprimedata[[i]][[j]][[k]] + (-4/
        time piprimedata[[i]][[j]][[k]] -
       2/time^2 pidata[[i]][[j]][[k]] -
       2/time (1/(
          8 meshsize^2) ((pidata[[
                 Floor[Mod[i + 1 - 1, 1/meshsize] + 1]]][[
                Floor[Mod[j - 1, 1/meshsize] + 1]]][[
               Floor[Mod[k - 1, 1/meshsize] + 1]]] -
              pidata[[Floor[Mod[i - 1 - 1, 1/meshsize] + 1]]][[
                Floor[Mod[j - 1, 1/meshsize] + 1]]][[
               Floor[Mod[k - 1, 1/meshsize] + 1]]])^2 + (pidata[[
                 Floor[Mod[i - 1, 1/meshsize] + 1]]][[
                Floor[Mod[j + 1 - 1, 1/meshsize] + 1]]][[
               Floor[Mod[k - 1, 1/meshsize] + 1]]] -
              pidata[[Floor[Mod[i - 1, 1/meshsize] + 1]]][[
                Floor[Mod[j - 1 - 1, 1/meshsize] + 1]]][[
               
               Floor[Mod[k - 1, 1/meshsize] + 1]]])^2 + (pidata[[
                 Floor[Mod[i - 1, 1/meshsize] + 1]]][[
                Floor[Mod[j - 1, 1/meshsize] + 1]]][[
               Floor[Mod[k + 1 - 1, 1/meshsize] + 1]]] -
              pidata[[Floor[Mod[i - 1, 1/meshsize] + 1]]][[
                Floor[Mod[j - 1, 1/meshsize] + 1]]][[
               Floor[Mod[k - 1 - 1, 1/meshsize] + 1]]])^2)) -
       1/(2*meshsize) (pidata[[Floor[
               Mod[i + 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k - 1, 1/meshsize] + 1]]] -
          pidata[[Floor[Mod[i - 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k - 1, 1/meshsize] + 1]]]) 1/(
        2*meshsize) (piprimedata[[Floor[
               Mod[i + 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k - 1, 1/meshsize] + 1]]] -
          piprimedata[[Floor[Mod[i - 1 - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k - 1, 1/meshsize] + 1]]]) -
       1/(2*meshsize) (pidata[[Floor[
               Mod[i - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k - 1, 1/meshsize] + 1]]] -
          pidata[[Floor[Mod[i - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k - 1, 1/meshsize] + 1]]]) 1/(
        2*meshsize) (piprimedata[[Floor[
               Mod[i - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j + 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k - 1, 1/meshsize] + 1]]] -
          piprimedata[[Floor[Mod[i - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j - 1 - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k - 1, 1/meshsize] + 1]]]) -
       1/(2*meshsize) (pidata[[Floor[
               Mod[i - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k + 1 - 1, 1/meshsize] + 1]]] -
          pidata[[Floor[Mod[i - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k - 1 - 1, 1/meshsize] + 1]]]) 1/(
        2*meshsize) (piprimedata[[Floor[
               Mod[i - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k + 1 - 1, 1/meshsize] + 1]]] -
          piprimedata[[Floor[Mod[i - 1, 1/meshsize] + 1]]][[Floor[
              Mod[j - 1, 1/meshsize] + 1]]][[Floor[
             Mod[k - 1 - 1, 1/meshsize] + 1]]]) -
       integral[[i]][[j]][[k]])*timestep, {i, 1, 1/meshsize}, {j, 1,
    1/meshsize}, {k, 1, 1/meshsize}]; time = time + timestep;
 pidata = pidatanext; piprimedata = piprimedatanext;
 AppendTo[pitimedata, {pidata, time}]; Print[t];]
