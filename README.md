# Tape for ELM 

`elm-non-empty-list` implements a non-empty sequence of elements which is useful in situations that we need 
to guarantee that a list of elements has at least one member. 

It uses the following type definition

    type NonEmpty = NonEmpty a (List a)  

which allows quick conversions between regular and non-empty lists and is part of the API.

NonEmpty follows a very similar API to ELM's builtin List module. It is not a drop-in replacement since some 
methods change signature. E.g., List.head returns a Maybe and NonEmpty return an element, since we know 
for sure that a head exist.
