# TerminalChart
get charts on terminal
It will take x and y values as an input and output a chart on the commandline
or to a file.
optional arguments:
  -h, --help            show this help message and exit
  -t TERMINAL TERMINAL, --terminal TERMINAL TERMINAL
                        append x and y values with the command if values are
                        short. Like -t '1,2,3' '3,2,3' or like -t '1 2 3' '3 2
                        3'
  -f FILE, --file FILE  add values in a file. like x: 1 2 3, y:3 2 3 or like
                        x: 1,2,3, y:3,2,3 and pass the input like: -f
                        input_file, recommended for large set of values
  -c CHARACTER, --character CHARACTER
                        pass the character you want to be displayed on chart,
                        will default to %& if none given
  -o OUTPUT, --output OUTPUT
                        where you want your output to be, -o t for terminal,
                        -o output_file for file

## Installation
~~~
pip3 install terminalchart
~~~

## Usage
### from commandline
~~~
python3 -m terminalchart -f file.txt -o output
~~~
with character
~~~
python3 -m terminalchart -f file.txt -o t -c 'c'
~~~

### from within python
~~~
from teminalchart import terminalchart as tc
tc(['-f', 'file.txt', '-o', 'output1'])
tc(['-f', 'file.txt', '-o', 'output1', '-c', 'c'])
tc(['-f', 'file.txt', '-o', 't'])
tc(['-f', 'file.txt', '-o', 't', '-c', 'c'])
~~~