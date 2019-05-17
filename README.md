# Simple LR Parser

(Displays the order of shift-reduce moves to parse a string)

## *Example* :

 For the given grammar
 
	S -> E
	E -> E+T | T
	T -> T*F | F
	F -> (E) | x

and string ```  x*x+x ``` . The output is

	x        Shift x
	F        Reduce F -> x
	T        Reduce T -> F
	T*       Shift *
	T*x      Shift x
	T*F      Reduce F -> x
	T        Reduce T -> T*F
	E        Reduce E -> T
	E+       Shift +
	E+x      Shift x
	E+F      Reduce F -> x
	E+T      Reduce T -> F
	E        Reduce E -> E+T
  Accepted :)
