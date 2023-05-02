Download Link: https://assignmentchef.com/product/solved-comp3350-hw-5-theme-data-definitions-addressing-modes-arrays
<br>
<ol>

 <li>[Memory Map] Fill in the following memory diagram with the data provided below. Please assume that the data segment begins at 0x0040400A.</li>

</ol>




.data

Alpha       WORD        0CDh, 1234h

Beta       BYTE        56h

Gamma       DWORD       01234ABCDh

Delta       BYTE        77h




<table>

 <tbody>

  <tr>

   <td width="105"><em>Address</em></td>

   <td width="77"><em>Variable</em></td>

   <td width="55"><em>Data</em></td>

  </tr>

  <tr>

   <td width="105">0040400A</td>

   <td width="77"><strong><em>Alpha</em></strong></td>

   <td width="55"><strong><em>CD</em></strong></td>

  </tr>

  <tr>

   <td width="105">0040400B</td>

   <td width="77"><strong><em> </em></strong></td>

   <td width="55"><strong><em>00</em></strong></td>

  </tr>

  <tr>

   <td width="105">0040400C</td>

   <td width="77"><strong><em> </em></strong></td>

   <td width="55"><strong><em>34</em></strong></td>

  </tr>

  <tr>

   <td width="105">0040400D</td>

   <td width="77"><strong><em> </em></strong></td>

   <td width="55"><strong><em>12</em></strong></td>

  </tr>

  <tr>

   <td width="105">0040400E</td>

   <td width="77"><strong><em>Beta</em></strong></td>

   <td width="55"><strong><em>56</em></strong></td>

  </tr>

  <tr>

   <td width="105">0040400F</td>

   <td width="77"><strong><em>Gamma</em></strong></td>

   <td width="55"><strong><em>CD</em></strong></td>

  </tr>

  <tr>

   <td width="105">00404010</td>

   <td width="77"><strong><em> </em></strong></td>

   <td width="55"><strong><em>AB</em></strong></td>

  </tr>

  <tr>

   <td width="105">00404011</td>

   <td width="77"><strong><em> </em></strong></td>

   <td width="55"><strong><em>34</em></strong></td>

  </tr>

  <tr>

   <td width="105">00404012</td>

   <td width="77"><strong><em> </em></strong></td>

   <td width="55"><strong><em>12</em></strong></td>

  </tr>

  <tr>

   <td width="105">00404013</td>

   <td width="77"><strong><em>Delta</em></strong></td>

   <td width="55"><strong><em>77</em></strong></td>

  </tr>

 </tbody>

</table>




<ol>

 <li>[Addressing Modes] Copy the following code into your assembly development environment and single-step through it.  For each single step execution, submit the screenshot.  For those instructions referencing memory, do the linear address computation (typewritten/handwritten).</li>

</ol>




TITLE Addressing Modes              (main.asm)

INCLUDE Irvine32.inc

.data

alpha       DWORD       10203040h, 50607080h

beta       DWORD       90A0B0C0h, D0E0F000h

gamma       DWORD       1234h




.code

main PROC

mov eax, ABCDh;               Immediate







mov ecx, eax;                 Register to Register







mov edi, OFFSET beta;         Immediate

Linear address: 00401017







mov [gamma], eax;             Indirect

Linear address: 0040101C







mov esi, [gamma];             Direct

Linear address: 00401021







mov esi, 4;                   Immediate







mov eax, beta[esi];           Indirect-offset

Linear address: 0040102C







mov ebx, OFFSET alpha;        Immediate

Linear address: 00401032







mov eax, [ebx];               Indirect

Linear address: 00401037







mov eax, 4[ebx];              Indirect-displacement

Linear address: 00401039







mov eax, 4[ebx][esi];         Base-Indirect-displacement

Linear address: 0040103C

exit

main ENDP

END main










<ol>

 <li>[Indirect addressing] Write a program that subtracts the corresponding elements of Array1 and Array2 and stores the results in Array3; e.g. for the 8<sup>th</sup> element, Array3 [7] ß Array1 [7] – Array2 [7].  Include commands to display the elements of all the arrays.  Submit screenshot of the displays of the elements of all the arrays.  You can use WriteInt or WriteHex to display the elements of the arrays.  Fill in Array1 and Array2 by your own 10 numbers each.</li>

</ol>




.data

Array1      BYTE 7h, …

Array2      BYTE 4h, …

Array3      BYTE 10 DUP (?)







<ol>

 <li>[Loops] Write a program to compute the sum of first <em>n</em> odd integers of a series.  <em>Sum = 1 +  3 + 5 +…</em> Your program must:</li>

</ol>




<ol>

 <li style="list-style-type: none;">

  <ol>

   <li>Prompt user for integer <em>n</em>,</li>

   <li>Read the value of <em>n</em> from user input</li>

   <li>Calculate <em>Sum</em>, and;</li>

   <li>Print <em>Sum</em> on screen.</li>

  </ol></li>

</ol>




Please use the “WriteInt” procedure, not “DumpRegs”. Other relevant procedures: “ReadInt” and “WriteString.” The calculation can be done in many ways, and all submissions that evidence proper programming practice are acceptable. In your homework submission, please embed both the code and one screen shot for <em>n = 15</em>.


