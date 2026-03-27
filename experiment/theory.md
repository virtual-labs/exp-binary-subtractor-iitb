IC 74LS83 is a 4-bit parallel binary adder chip. It adds/subtracts a four-bit number (nibble) with another 4-bit number. The block symbol for the IC is shown in Fig.1. This IC has two sets of 4-bit inputs along with a carry input C0. It performs binary subtraction on the A &amp; B inputs and the carry input C0. It generates a 4-bit Difference and a Borrow out C4.

<center>
<img src="images/image001.png">
<br/>
<span >Fig. 1 Block Symbol of four-bit Subtractor IC </span><br/></center>


<span >A circuit that can subtract 4-bit numbers can be designed using a control input and additional EX-OR IC 74LS86 &nbsp;For this we use the EX-OR gate as a &ldquo;Controlled Inverter&rdquo;. The explaination for this concept can be easily understood from Fig.2. The four bit input B4, B3, B2 &amp; B1 can be passed through the controlled inverter IC74LS83 and the A4, A3, A2 &amp; A1 are connected directly to A inputs of IC 74LS83 as shown in Fig 3. </span>

<center>
<img src="images/image002.png">
<br/>
<span >Fig.2. Exclusive-OR gate used as a Controlled Inverter </span><br />
</center>
<br/>

<center>
<img src="images/image003.png">
<br/>
<span >Fig.3. 4-bit Binary Subtractor </span></center>

<strong><span >Four-bit Subtraction: </span></strong><span >When Control input is set = 1, the Carry &ndash;in input C0 = 1. In this situation, the Ex-OR gates will provide 1,&rsquo;s complement of the Input-2 to the B-inputs of Adder IC. Moreover as C0 = 1, the addition of 1 to the 1&rsquo;s complement of B gives 2&rsquo;s complement of B.</span><span >Now the IC74LS83 adds Input-1 i.e. A4,A3, A2,A1 to the 2&rsquo;s complemet of B and produces the Carry and Sum output on C4 &amp; the lines &Sigma;4, &Sigma;3, &Sigma;2, &amp; &Sigma;1.</span><br/><br/><strong><em><span ><span >Example</span></span></em></strong><strong><span ><span >1</span></span></strong><em><span ><span >:</span></span></em><span ><span > Let Input-1 = A4 A3 A2 A1 = 1001 &amp; Input-2 = 0111 &amp; control input be set to 1.</span></span><span >1&rsquo;s complement of 0111 = 1000. Since carry input C0 = 1, the input B becomes,</span></span><br/><span ><span >B4 B3 B2 B1 = 1000 + 1 = 1001.</span></span><br/><span ><span >Now IC 74LS83 performs addition of A &amp; 2,s complement of B and produces the output. </span></span><center><img src="images/image005.png"><br/></center><br/><span ><span >Since a Carry is generated <em>discard the Carry</em> and the Sum is the final output of subtraction operation.</span></span><br/><span ><span >The result is &Sigma;4 &Sigma;3 &Sigma;2 &amp; &Sigma;1 = 0 0 1 0.</span></span><br/><br/><em><span ><span ><b>Example</b></span></span></em></strong><strong><span ><span >2</span></span></strong><em><span ><span >:</span></span></em><span ><span > Let Input-1 = A4 A3 A2 A1 = 0111 &amp; Input-2 = 1001 &amp; control input be set to 1.</span></span><br/><span ><span >1&rsquo;s complement of Input-2 i.e. 1001 = 0110&nbsp; Since carry input C0 = 1, the input B becomes,</span></span><br/><span ><span >B4 B3 B2 B1 = 0110 + 1 = 0111.</span></span><br/><span ><span >Now IC 74LS83 performs addition of A &amp; 2&rsquo;s complement of B and produces the output. </span></span><center><img src="images/image006.png"><br/></center><br/><span ><span >In this case <em>no Carry</em> is generated during addition. Hence the answer can be obtained by taking the <em>2&rsquo;s complement</em> of the Sum output and <em>attaching a negative sign.</em></span></span><span ><span >So the 2&rsquo;s complement of 1110 = 0010 and the final result of subtraction </span></span><span ><span >is </span></span><span ><span >&Sigma;4 &Sigma;3 &Sigma;2 &amp; &Sigma;1 = - 0 0 1 0.</span></span>&nbsp;&nbsp;&nbsp;</div>

#### Numerical:

<p class=MsoNormal><span >For subtracting two number, the 2&#39;s complement of
one number is calculated and then added to other number</span></p>

<p class=MsoNormal><span >To calculate 2&#39;s complement of a number, the 1&#39;s
complement of number is calculated i.e. number is represented in binary format,
and then inverted. And then add 1 to it.</span></p>

<p class=MsoNormal><span >For <span class=SpellE><span class=GramE>eg</span></span><span
class=GramE>.:</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Complement of 2
is:</span></p>

<p class=MsoNormal><span >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
=&gt;&nbsp;&nbsp;&nbsp;&nbsp; 0010</span></p>

<p class=MsoNormal><span >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
1&#39;s complement&nbsp;&nbsp;&nbsp;&nbsp; =&gt;&nbsp;&nbsp;&nbsp;&nbsp; 1101</span></p>

<p class=MsoNormal><span >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
2&#39;s complement&nbsp;&nbsp;&nbsp;&nbsp; =&gt;&nbsp;&nbsp;&nbsp;&nbsp; 1101<span
class=GramE>&nbsp; +</span> 1&nbsp;&nbsp;&nbsp;&nbsp; =&gt; 1110</span></p>

<p class=MsoNormal><span >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Hence 2&#39;s complement of 2 is 1110.</span></p>

<p class=MsoNormal><span >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></p>

<p class=MsoNormal><span >Examples:</span></p>

<p class=MsoListParagraph ><span >1.</span><span
>&nbsp;&nbsp;&nbsp;&nbsp;
</span><span >&nbsp;&nbsp;&nbsp;&nbsp;1.&nbsp;&nbsp;4
- 0</span></p>

<p class=MsoListParagraph><span >&nbsp;</span></p>

<p class=MsoListParagraph ><span >2&#39;s Complement
of&nbsp;&nbsp; 0<span class=GramE>&nbsp; =</span>&nbsp; 1 0000</span></p>

<p class=MsoListParagraph><span >&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=0 cellpadding=0
 >
 <tr >
  <td width=25 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;</span></p>
  </td>
  <td width=168 valign=top >
  <p class=MsoListParagraph ><span>4</span></p>
  </td>
  <td width=17 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
 </tr>
 <tr >
  <td width=25 valign=top s>
  <p class=MsoListParagraph ><span>+</span></p>
  </td>
  <td width=168 valign=top >
  <p class=MsoListParagraph ><span>2&#39;s
  complement of 0</span></p>
  </td>
  <td width=17 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
 </tr>
 <tr >
  <td width=25 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;</span></p>
  </td>
  <td width=168 valign=top >
  <p class=MsoListParagraph ><span>4</span></p>
  </td>
  <td width=17 valign=top >
  <p class=MsoListParagraph align=center><span >1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
 </tr>
</table>

<p class=MsoListParagraph><span >&nbsp;<span> </span><o:p></o:p></span></p>

<p class=MsoListParagraph><span >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(The
MSB bit is complemented to achieve the Sign-bit)</span></p>

<p class=MsoListParagraph><span >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Sign Bit = 0<span> </span>(Positive Number)</span></p>

<p class=MsoListParagraph><span >&nbsp;</span></p>

<p class=MsoListParagraph><span >&nbsp;</span></p>

<p class=MsoListParagraph ><span >2.</span><span
>&nbsp;&nbsp;&nbsp;&nbsp;
</span><span >&nbsp;&nbsp;&nbsp;&nbsp;2.&nbsp;&nbsp;4
- 2</span></p>

<p class=MsoListParagraph><span >&nbsp;</span></p>

<p class=MsoListParagraph ><span >2&#39;s Complement
of&nbsp;&nbsp; 2<span class=GramE>&nbsp; =</span>&nbsp; 0 1110</span></p>

<p class=MsoListParagraph><span >&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=0 cellpadding=0
 >
 <tr >
  <td width=25 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;</span></p>
  </td>
  <td width=168 valign=top >
  <p class=MsoListParagraph ><span>4</span></p>
  </td>
  <td width=17 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
 </tr>
 <tr >
  <td width=25 valign=top s>
  <p class=MsoListParagraph ><span>+</span></p>
  </td>
  <td width=168 valign=top >
  <p class=MsoListParagraph ><span>2&#39;s
  complement of 2</span></p>
  </td>
  <td width=17 valign=top >
  <p class=MsoListParagraph align=center><span >0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
 </tr>
 <tr >
  <td width=25 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;</span></p>
  </td>
  <td width=168 valign=top >
  <p class=MsoListParagraph ><span>2</span></p>
  </td>
  <td width=17 valign=top >
  <p class=MsoListParagraph align=center><span >1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
 </tr>
</table>

<p class=MsoListParagraph><span >&nbsp;</span></p>

<p class=MsoListParagraph><span >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sign
Bit = 0<span> </span>(Positive Number)</span></p>

<p class=MsoListParagraph><span >&nbsp;</span></p>

<p class=MsoListParagraph ><span >3.</span><span
>&nbsp;&nbsp;&nbsp;&nbsp;
</span><span >&nbsp;&nbsp;&nbsp;&nbsp;3.&nbsp;&nbsp;2
- 4</span></p>

<p class=MsoListParagraph><span >&nbsp;</span></p>

<p class=MsoListParagraph ><span >2&#39;s Complement
of&nbsp;&nbsp; 4<span class=GramE>&nbsp; =</span>&nbsp; 1100</span></p>

<p class=MsoListParagraph><span >&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=0 cellpadding=0
 >
 <tr >
  <td width=25 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;</span></p>
  </td>
  <td width=168 valign=top >
  <p class=MsoListParagraph ><span>2</span></p>
  </td>
  <td width=17 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
 </tr>
 <tr >
  <td width=25 valign=top s>
  <p class=MsoListParagraph ><span>+</span></p>
  </td>
  <td width=168 valign=top >
  <p class=MsoListParagraph ><span>2&#39;s
  complement of 4</span></p>
  </td>
  <td width=17 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
 </tr>
 <tr >
  <td width=25 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;</span></p>
  </td>
  <td width=168 valign=top >
  <p class=MsoListParagraph ><span>14</span></p>
  </td>
  <td width=17 valign=top >
  <p class=MsoListParagraph ><span>&nbsp;0</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>1</span></p>
  </td>
  <td width=24 valign=top >
  <p class=MsoListParagraph ><span>0</span></p>
  </td>
 </tr>
</table>

<p class=MsoListParagraph><span >&nbsp;</span></p>

<p class=MsoListParagraph><span >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sign
Bit = 1<span> </span>(Negative Number)<o:p></o:p></span></p>

<p class=MsoListParagraph><o:p>&nbsp;</o:p></p>

<p class=MsoNormal><span> </span><span
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;As
the output is negative number, it is in the 2&#39;s complement format. Hence the
2&#39;s <span class=GramE>complement of Answer need</span> to be taken, to achieve
the right answer:<o:p></o:p></span></p>

<p class=MsoNormal><span ><span > </span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Answer<span
> </span>=&gt;<span > </span>1110<o:p></o:p></span></p>

<p class=MsoNormal><span ><span > </span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1&#39;s
Complement <span> </span>=&gt;<span > </span>0001<o:p></o:p></span></p>

<p class=MsoNormal><span >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2&#39;s
Complement<span> </span>=&gt;<span > </span>0001 + 1 = 0010<o:p></o:p></span></p>

<p class=MsoNormal><span >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Hence,
final answer = 0010<span> </span>with Sign bit =
1<o:p></o:p></span></p>



<script type="text/javascript" id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"> </script>