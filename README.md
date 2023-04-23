Download Link: https://assignmentchef.com/product/solved-assignment-3-ee-l4732-5733-advanced-system-programming
<br>
In this assignment, you are going to simulate electronic fund transfer (EFT) between bank accounts. We will assume that there is just one bank and several accounts. Your program will take an input file in the form

Acco u nt N o 1 &lt; space&gt; initialBalance1

Acco u nt N o 2 &lt; space&gt; i n iti a l Ba l a n ce2

. .

Acco u nt N o N &lt;space&gt; i n i ti a l Ba l a n ce N

Transfer &lt;space&gt; accountNoFrom1 &lt;space&gt; accountNoTo1 &lt;space&gt; Amount1 Transfer &lt;space&gt; accountNoFrom1 &lt;space&gt; accountNoTo2 &lt;space&gt; Amount2 …

Transfer &lt;space&gt; a cco u n t N o F ro m 1 &lt; space&gt; a cco u n t N oTo 1 &lt;space&gt; Am o u nt 1

which first lists the accounts in the system along with the initial balances and then lists the transfers between accounts. You can assume that all transfers refer to existing accounts and all initial balances and the transfer amounts are n o n n egative integers.

Your program should take one more parameter to denote the number of worker threads that will run in parallel. Note that the main thread will initialize the accounts, read the input file and assign work (EFTs) to worker threads in a round-robin fashion until all transfers are processed. It is possible that an account may be overdrawn and gets a negative value while processing. Your program should output on the standard output the amount in each account (in the order specified in the input file) once all transfers are computed.

Usage of your program:

$ transfProg inputFile numWorkers

So, as an example, assuming the input file is as below

1 1000

250

3 40 0

4 1 5 0

<table>

 <tbody>

  <tr>

   <td width="83">Transfer 1</td>

   <td width="12">2</td>

   <td width="538">200</td>

  </tr>

  <tr>

   <td width="83">Transfer 1</td>

   <td width="12">4</td>

   <td width="538">50</td>

  </tr>

  <tr>

   <td width="83">Transfer 2</td>

   <td width="12">3</td>

   <td width="538">100</td>

  </tr>

 </tbody>

</table>

<table width="635">

 <tbody>

  <tr>

   <td>your program should produce the following output regardless of the number of worker threads specified:</td>

  </tr>

 </tbody>

</table>

1 7502 1503 5004 200To get full credit, your solution should maximize concurrency, be free of race conditions anddeadlocks, and produce the correct output. You can use mutexes and condition variablesand/or semaphores for synchronizing your threads. Please submit your files (source, README,and a Makefile) on CANVAS by the due date.