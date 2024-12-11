java c
Abstract Data Types and Algorithms
COMP 2402 ABC -   Fall 2024
Assignment 5
Due: Tuesday,   December 3, 23:59
Download the   Provided   Files
The   base code for this assignment consists of   one   zip   file,   which you   can   download   from   Brightspace:   comp2402a5.zip - source code. This file contains a folder   named   comp2402a5   with   five   .java   files:
•          AdjacencyLists.java
•          Algorithms.java
•            Graph.java
•          MixAndBoom.java   - add   your   code   here
•          SnakesAndLadders.java   - add   your   code   here
Start   by   reviewing the skeleton code.   Unlike the   previous three assignments, this   one   does   NOT   include   a slow   (correct)   implementation.   However,   a custom-made Graph   interface   is   provided, along with the   associated classes AdjacencyLists   and Algorithms. The Algorithms   class contains   useful methods that can assist you with your   assignment.
Additionally, you are also   provided with sample   input and   output   files,   available   as   a   zip file:   a5-io.zip.
Use these files to familiarize yourself with testing your code.   Once you   understand   how to   work   with   the   provided   input and output files, create your own tests to   thoroughly   evaluate   your   program.   Note   that the   provided tests are   not exhaustive and   are   meant to serve   as   a   starting   point.
Grading
This assignment will   be tested and graded   by a   computer   program   also   known   as   an   auto-grader. You   can submit as   many times as you   like; your   highest grade   is   recorded.   For this to   work,   there   are   some   important   rules you   must   follow:
•          Keep the   directory   structure   of the   provided   comp2402a5.zip file.   If you find   a   file   in   the   subdirectory   comp2402a5   leave   it there.
•          Keep the   package structure   of the   provided   zip   file.   If   you   find   a      package comp2402a5;   directive at the top of a   .java   file,   leave   it   there.
•          Keep the   interfaces as   they   are.   You   may   add   internal   methods   to   your   implementation,   but   do   not   introduce any   new   methods to the   interfaces.
•          Do   not   rename or   change   the   visibility   of   any   methods   already   present.   If   a   method   or   class   is   public,   leave   it that way.
•          Submit early and   often. The   auto-grader   will   compile   and   run   your   code,   providing   you   with instant feedback and a grade. You can   submit   as   many   times   as you   like   –   your   final   grade   will   reflect your   last submission. Alternatively, you can choose to   activate your   highest-graded
submission as your final score. With this flexibility, there’s   no excuse   for   submitting   code   that   doesn’t compile or fail   the tests.
•          The assignment consists of two   independent   parts,   each   of   which   will   be   graded   separately   by   the auto-grader.
•          The goal for this assignment   is to   write   efficient   code.   If you   select   and   implement   your   data   structures correctly, your code will execute efficiently within   the   time   and   memory   limits.
However,   if you choose   inappropriate data structures or   misuse them,   your   code   may   run   too   slow to   be graded   by the auto-grader,   resulting   in a grade   of   0.
•          The auto-grader   places a time   limit   on   how   long   it   will   be   executing   your   code,   often   testing with over a   million elements and   operations.
•            Memory   usage   is also capped.
Submitting and Testing
Submitting to Gradescope   is simple: drag and   drop   ALL   your   .java files   into   the   submission   window   provided.   If you encounter any   issues,   please   post them on   Discord so the teaching   team   (or   your classmates) can assist you.   Including screenshots can   help   resolve   problems   more   quickly.
When you submit your code, the auto-grader   runs   numerous tests   on   it.   We   will   not   disclose the tests used   by the auto-grader,   because you should try to find   exhaustive tests   of your   own   code.   You   are   encouraged to create your own tests and test   locally   before trying your   submission   on   Gradescope.   Keep   in   mind that the auto-grader   has a strict time   limit of   5   seconds   pertest   case.   Any   test   that   exceeds   this         limit will   be   marked as failed, and subsequent tests for   that   part   will   not   be   executed.   For   larger   test   cases, even an optimal   implementation   may take   up to   3 seconds,   and this   time   could   increase   if the   server   is   heavily   loaded. To avoid   potential   issues,   please   begin submitting your assignment well   in advance of the   deadline.
Start   by downloading and decompressing the Assignment 5   Zip   File   (comp2402a5.zip),   which   contains   a         skeleton of the code you   need to write. The skeleton   code   in the   zip file   compiles   fine.   You   can   unzip   the   file   (extract   its content)   in   numerous ways, such as   by drag-and-drop   or   right-mouse-click “Extract   all”   .               Here's what   it   looks   like when you   unzip and compile   it from   the   command   line   (the   commands   that   you   type are   highlighted   in yellow):
>   unzip   comp2402a5.zip
Archive:    comp2402a5.zip
inflating: comp2402a5/AdjacencyLists.java   inflating: comp2402a5/Algorithms.java
inflating: comp2402a5/   Graph.java
inflating: comp2402a5/MixAndBoom.java
inflating: comp2402a5/   SnakesAndLadders.java   >   javac   comp2402a5/*.java
Here   is an example of   how to   use command-line arguments   to   do   your   own testing.   Make   sure   your
terminal is open   in the folder that contains the   folder   comp2402a5   with   your   .java   files.   Add   your   input   test file, for example   part1-1.in, to the folder your terminal   is   in.
>   java comp2402a5.MixAndBoom   part1-1.in   yes
Execution time:   0.0017132
This way, you do   not   need to type   input   line   by   line,   but   rather   provide   it as   a file   via   command-line   arguments.   Now you can compare your output to the correct   output   provided   in   part1-1.out   file.
If you are   having trouble   running these   programs, figure this out first   before   attempting to   do   the   assignment.   If you are stuck, ask on   Discord,   and our   teaching   team   or   another   student   will   likely   help   you fairly   quickly.
The Assignment
This assignment consists of two   main   parts:
•          For   part   1,   implement the   doIt()   method   in the   MixAndBoom   class.
•          For   part 2,   implement the   doIt()   method   in   the   代 写COMP 2402 ABC - Fall 2024 - Abstract Data Types and Algorithms Assignment 5Java
代做程序编程语言SnakesAndLadders   class.
To   assist you, a custom Graph   interface   has   been   provided, along with   its   related   classes
(AdjacencyLists   and Algorithms). You   might find these classes   helpful. Also, you are welcome   to   modify some of the   methods from Algorithms   and   use them   in your solution.
Part   1:   Mix And   Boom   [50 marks]   Professor   Mixiten   Kaboom   is a famous chemist   who   is   constantly inventing   new chemicals.   Unfortunately, for some strange   reason, some   of   his   chemicals   tend to   explode when   mixed with some of the other   chemicals. To   make   things   even   worse,   he   has   only   two   storage compartments   in   his   lab. The only way to store the   chemicals   safely   is   to   divide   them   between   the compartments so that   no two chemicals that explode   when   mixed   arestored   in   the   same   compartment.   Earlier, when the   number of chemicals was small, the   professor   could   do   it   easily.   But   now that   he   has accumulated so   many chemicals over the   years,   the   task   has   become   too   time-   consuming.   He asks for your   help solving this   problem. Given   N chemicals   and   a   list   of   chemical   pairs
that explode when   mixed, you will   have to write a   program   that   determines   if   it   is   possible to   store   them   using the two storage compartments.
The   input   begins with an   integer   in a   single   line, which   is the   number   of   chemicals the   professor   has. The   chemicals are   numbered from   1 to   N.   Next, there   is a sequence   of   lines,   each   containing   a   pair   of         integers   (between   1 and   N   inclusive),   representing two chemicals that explode   when   mixed.   If   it   is   possible to store the chemicals   safely, your   program should   output “yes”,   and “no”   otherwise.Part 2: Snakes And   Ladders   [50   marks] A worldwide classic   boardgame.   Navigate your token   from   start      to finish, avoid the snakes   (something you should   consider)   and take   shortcuts   going   up the   ladders.   The   board   is a grid of squares   numbered from   1 to   the   final   square.   For   our   assignment,   assume   the   board   is      an   N-by-N   matrix.
The   rules of the   boardgame   "Snakes and   Ladders" are simple:
•          Each   player starts   at   location   1   and takes   turns   to   move   their   token   forward.
•          Players take turns   rolling   a   six-sided   dice to   determine   how   many   squares   they   will   move   on   their turn.
•          Move your token forward   along   the   board   the   number   of   squares   shown   on   the   dice.
•          If your token   lands   on   asquare   at the   base   of   a   ladder, you   can   immediately   climb   the   ladder   to   the square   at the   top.
•          If your token   lands   on   a   square   with the   mouth   of   a   snake, you   must   slide   down   to   the   square   at   the snake's   tail.
•          The first   player to   reach or exceed the   final   square   is   the   winner   of the   game.
Imagine that you   have a   magical six-sided dice   that   rolls   any   number you   want   between   1   and   6.   Given   a   board of size   N-by-N, a configuration of   snakes   and   ladders,   and   the   magical   six-sided   dice, you   must determine the   minimum   number of dice   rolls you will   need togo from   location   1 to   location   N*N.
The   input   begins with an   integer   in a single   line, which   represents the   board   dimension   N.   Next,   there   is   a sequence of   lines, each containing   a   pair of   integers   (between   1   and   N*N   inclusive),   representing
either   aladder   or   a   snake. A   ladder is   represented   by a   pair where the      first   number   is smaller than the
second, and the opposite   for   snakes.
You   may assume that   no   ladder
starts at the first   square   (1),   and   no   snake starts at   the   last   square
(N*N).Your   program should output   a      single   integer   representing the   minimum   number of dice   rolls      required to   reach the   location      N*N.
Example of the   board   
Tips,Tricks, and   FAQs
Take time to   plan your solution carefully   before starting to   code.   Here   are   some tips   to   guide you:
•          You   may   have already figured out   that   this   assignment   revolves   around   graphs.   Consider   how   each   problem can   be framed as a graph   problem, then   design   an   algorithm   to   solve   it.
•          Sketch a sample   graph   and   manually   simulate your   algorithm   step   by   step.   Test   it   on   different   examples to ensure   it works   in   all   cases.
•          Once confident   in your   algorithm,   begin   implementation. The   provided   Graph   class   is   a   great   starting   point for testing, - some   basic algorithms are   already   included for   reference.
•          You can save   memory   usage   by   NOT   storing   unnecessary   information when the   graph   is   sparse.
How should   Itest   my code?
For this assignment, you will   have to test your own code thoroughly.   The   auto-grader   will   perform   a
range of tests on your   implementation,   but   it does   not give   much   information   when things   go   wrong.            The auto-grader cannot determine   logical errors from   crash   reports,   and   the   responsibility   falls   on the      programmer. You are advised to write your own   tests   and test   your   code   locally,   where   you   have   more   control over debugging your   code.
•          Use the   sample   input/output files   as   a   starting   point to   understand   the   required   format.   Then,   make your own   input files and test your solutions   with   them.
•          Test for   both correctness and   speed.   Write the   correct   code   first,   and   then   focus   on   optimizing   its   speed.
•          All the tests on the   server   are   heavily   memory   constrained.   Be careful   with   how   much   memory   your solution takes.
•          In some   cases, your   solution   maybe   acceptably   fast   but   too   memory-intensive,   which   may   lead   to timeout   because of   how the JVM garbage collector   behaves on the   server.
•          Test   incrementally. Start with small, simple testcases   that   can   be   solved   manually.   Gradually       increase the complexity to   include   edge cases,   large   inputs,   empty   inputs, and   random   inputs.
•          Avoid   leaving   unnecessary debugging   print statements   (System.out)   in your   code. These   can   slowdown execution or cause   crashes   if the output   is too   large.   Remove them   before submitting your work to the auto-grader.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
