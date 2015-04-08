# handy-rpn

A Handy (see what I did there) Reverse Polish Notation Calculator!

To run tests:

   git clone https://github.com/slabgorb/handy-rpn.git
   cd handy-rpn
   bundle install
   bundle exec rspec

To run application:

   git clone https://github.com/slabgorb/handy-rpn.git
   cd handy-rpn
   ./handy-rpn




From Wikipedia: http://en.wikipedia.org/wiki/Reverse_Polish_notation

*   While there are input tokens left
    *   Read the next token from input.
    *   If the token is a value
        *   Push it onto the stack.
    *   Otherwise, the token is an operator (operator here includes both operators and functions).
        *   It is known that the operator takes **n** arguments.
        *   If there are fewer than **n** values on the stack
            *   **(Error)** The user has not input sufficient values in the expression.
        *   Else, Pop the top **n** values from the stack.
        *   Evaluate the operator, with the values as arguments.
        *   Push the returned results, if any, back onto the stack.
*   If there is only one value in the stack
    *   That value is the result of the calculation.
*   Otherwise, there are more values in the stack
    *   **(Error)** The user input has too many values.
