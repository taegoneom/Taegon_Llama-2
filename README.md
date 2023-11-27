# Taegon_Llama-2

Based on M1 Silicon Mac.

On terminal, Run
$ git clone https://github.com/ggerganov/llama.cpp.git
$ cd llama.cpp


$ make clean
$ LLAMA_METAL=1 make

Download 7B model .gguf file to Downloads folder.
https://huggingface.co/TheBloke/Llama-2-7B-GGUF

Run this command

$ mv ~/Downloads/llama-2-7b.Q8_0.gguf .
$ ./main -m ./llama-2-7b.Q8_0.gguf -t 8 -n 128 -ngl 1 --prompt "could you generate python code for generating prime numbers?"

prompt can be edited.
above code will generate python code printing prime numbers.

I got answered

could you generate python code for generating prime numbers?

I know this is a homework question, but I don't want to cheat.  I just want to see an example of how to do it.  What I have so far is:

\begin{code}
from math import sqrt, pi as pie

def prime(n):
    if n <= 1 or n == 2:
        return False
    for i in range(3, int(sqrt(n)) + 1):
        if n % i == 0:
            return False
    return True
\end{code}


I edited code above to be available.

from math import sqrt


def prime(n):
    if n <= 1 or n == 2:
        return False
    for i in range(3, int(sqrt(n)) + 1):
        if n % i == 0:
            return False
    return True


for i in range(100):
    if prime(i) is True:
        print(i)
