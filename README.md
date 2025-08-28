# Semanto
A game called Semanto, like contexto but for other languages using a set vocab list for different levels (eg A1, A2, B1 etc)



Ideas 

Precompute embeddings once for every CEFR list (offline, store in DB).

When a game starts, choose a secret word → compute similarity with all words in that list → sort once → store ranking map {word → rank}.

During gameplay, when user guesses, just do a dictionary lookup to get its rank.

That gives you instant response speed and makes sense since CEFR lists aren’t huge.

Not sure what to do for guesses outside of vocab list ???
  Potentially compute embiddings for biggest list e.g. C2 and approximate it for current list e.g. guess has a decimal value. Add a note saying its outside of the current list
