<HTML>
<H1>Adjusted Charge Partitioning and Iterative Adjusted Charge Partitioning</H1>
<H2>Introduction</H2>
<P>Atomic charge schemes, dubbed <I>Adjusted Charge Partitioning</I> (ACP)
and <I>Iterative Adjusted Charge Partitioning</I> (I-ACP), are based on a
Hirshfeld-like scheme in which weighting factors <I>c<SUB>A</SUB></I>
<I>r</I><SUP>2<I>n</I>&ndash;2</SUP>exp(&ndash;<I>&alpha;</I><SUB><I>A</I></SUB><I>r</I>)
are used to partition the valence molecular electron density into atomic components.
In the ACP method, both parameters <I>&alpha;</I><SUB><I>A</I></SUB> and <I>c<SUB>A</SUB></I>
are pre-defined. In the I-ACP method only <I>&alpha;</I><SUB><I>A</I></SUB> is fixed, while
<I>c<SUB>A</SUB></I> is determined iteratively in every calculations.

Built-in parameters are available for 17 main-group elements H, Li to F, Na to Cl,
Br, and I. In addition, in the case of the I-ACP method, the
<I>&alpha;</I><SUB><I>Ti</I></SUB> is available for titanium. Users are free to
introduce and to use their own parameters for any element.

<P>The ACP scheme is non-iterative, therefore simple and
reliable. The I-ACP scheme is more flexible and equally reliable,
but the calculation is slightly more expensive. Both ACP and I-ACP are
specifically designed for the resulting atomic charges to accurately
reproduce the molecular dipole moment.</P>

<P>The ACP atomic charges can be calculated by the program <FONT FACE="Courier">ACP</FONT>:
<br><A HREF="./ACP.exe">ACP.exe</A> &ndash; Windows version
<br><A HREF="./ACP.x">ACP.x</A> &ndash; Linux version</P>

<P>Similarly, the program <FONT FACE="Courier">I-ACP</FONT> serves to calculate the Iterative ACP charges:
<br><A HREF="./I-ACP.exe">I-ACP.exe</A> &ndash; Windows version
<br><A HREF="./I-ACP.x">I-ACP.x</A> &ndash; Linux version</P>

Both programs can be downloaded here free of charge

<P>Once you use any results calculated by the <FONT FACE="Courier">ACP</FONT>
or <FONT FACE="Courier">I-ACP</FONT> programs, you have to include the following citations:
<br>For the <FONT FACE="Courier">ACP</FONT> program:
<br><b>1</b>. S.F.Vyboishchikov, ACP program, Girona, <B>2018</B>
<br><b>2</b>. A.A.Voityuk, A.J.Stasyuk, S.F.Vyboishchikov, &quot;A simple
model for calculating atomic charges in molecules&quot;
<A HREF="https://pubs.rsc.org/en/content/articlelanding/2018/cp/c8cp03764g"><I>PCCP</I>,
<B>2018</B>, <I>20</I>, 23328&ndash;23337</A>, DOI: 10.1039/c8cp03764g</P>




For the <FONT FACE="Courier">I-ACP</FONT> program:
<br><b>1</b>. S.F.Vyboishchikov, I-ACP program, Girona, <B>2018</B>
<br><b>2</b>. S.F.Vyboishchikov, A.A.Voityuk, &quot;Iterative atomic-charge
partitioning of valence electron density&quot;
<A HREF="https://onlinelibrary.wiley.com/doi/10.1002/jcc.25771">
<i>J. Comp. Chem.</i>, <b>2019</b>, <i>40</i>, 875&ndash;884</A>,
DOI: 10.1002/jcc.25771</P>

<p>Questions related to the ACP and I-ACP methods should be addressed to
<A HREF="mailto:alexander.voityuk@gmail.com">Alexander Voityuk</A>
or <A HREF="mailto:vyboishchikov@googlemail.com">Sergei Vyboishchikov</A>. 
Specific questions about the programs should be addressed to 
<A HREF="mailto:vyboishchikov@googlemail.com">Sergei Vyboishchikov</A>.

<H2>Program use</H2>

<P>The programs use a Gaussian WFN file produced
by the Gaussian option <FONT FACE="Courier">OUTPUT=WFN</FONT>
and is invoked from a Linux or Windows command line interpreter as follows:
<br>For the <FONT FACE="Courier">ACP</FONT> program:
<br>&nbsp; <FONT FACE="Courier">ACP.exe file.wfn</FONT>
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; or
<br>&nbsp; <FONT FACE="Courier">ACP.exe file.wfn
[[&lt;option&gt; &lt;parameter&gt; ]&nbsp;&nbsp; [&lt;option&gt;
&lt;parameter&gt; ...&nbsp; ]]</FONT></P>
For the <FONT FACE="Courier">I-ACP</FONT> program:
<br>&nbsp; <FONT FACE="Courier">I-ACP.exe file.wfn</FONT>
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; or
<br>&nbsp; <FONT FACE="Courier">I-ACP.exe file.wfn
[[&lt;option&gt; &lt;parameter&gt; ]&nbsp;&nbsp; [&lt;option&gt;
&lt;parameter&gt; ...&nbsp; ]]</FONT></P>

<P>Here <FONT FACE="Courier">file.wfn</FONT> is a WFN file name.</P>

<P>&nbsp; Options:
<br>&nbsp;&nbsp;&nbsp; <FONT FACE="Courier">-r</FONT>
<I>radial_grid</I>
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<I>radial_grid</I> is the number of radial gridpoints per atom (default: 120)</P>

<P>&nbsp;&nbsp;&nbsp; <FONT FACE="Courier">-a</FONT>
<I>angular_grid</I>
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

<I>angular_grid</I> is the number of angular gridpoints per atom (default: 302)</P>

<P>&nbsp;&nbsp;&nbsp; <FONT FACE="Courier">-user</FONT>
<I>element_number </I><I>&alpha;</I><SUB><I>A</I></SUB>
<I>c</I><SUB><I>A</I></SUB>&nbsp;
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This
option serves to define or re-define <I>&alpha;</I><SUB><I>A</I></SUB>
and <I>c</I><SUB><I>A</I></SUB> parameters for element <I>element_number</I>.
In the case of the I-ACP method, the <I>c</I><SUB><I>A</I></SUB> parameter
has to be omitted.

The <FONT FACE="Courier">-user</FONT> option can be repeated for as many elements as
needed.</P>
</BODY>
</HTML>
