Download Link: https://assignmentchef.com/product/solved-ie523-homework-4-computing-the-general-solution-to-ax-y
<br>
I want you to write a generic solver for a set of simultaneous equations <strong>Ax </strong>= <strong>y</strong>, where <strong>A </strong>is a known <em>n </em>× <em>m </em>matrix and <strong>y </strong>is a known <em>n </em>× 1 vector. You may wish to look at lesson 2 of my notes for the relevant theory. <strong>This assignment can take some time, please get started on it ASAP</strong>. Here are the components your code:

<ol>

 <li>Check if there is a solution to <strong>Ax </strong>= <strong>y </strong>by testing if <em>rank</em>([<strong>A </strong>| <strong>y</strong>]) = <em>rank</em>(<strong>A</strong>).</li>

 <li>If there is no solution – report it as such. If there is a solution, then present the general solution to <strong>Ax </strong>= <strong>y</strong>.</li>

</ol>

You will need <em>NEWMAT </em>for this programming exercise. You might wish to look at linear algebra1.cpp, linear algebra2.cpp and linear algebra3.cpp on Compass to get started on this exercise. As you will see when you do this assignment (or, if you attended class regularly and listened attentively), you will need to pick <em>rank</em>(<strong>B</strong>)-many columns from a matrix <strong>B</strong>, at various instants. For this, you may wish to look at the C++ code provided with this assignment that computes <em>n-take-k </em>combinations of a set of <em>n </em>objects (where 1 ≤ <em>k </em>≤ <em>n</em>).

If there is a solution to <strong>Ax </strong>= <strong>y</strong>, you will have to compute all possible basic solutions, where you pick <em>rank</em>(<strong>A</strong>)-many columns of <strong>A </strong>(call this matrix <strong>X</strong>; <em>rank</em>(<strong>X</strong>) = <em>rank</em>(<strong>A</strong>)) and then compute <strong>z </strong>according to equation 1 of lesson 2 of my notes. You then have to insert zeros into <strong>z </strong>at appropriate locations (depending on which columns of <strong>A </strong>where chosen to be in <strong>X</strong>). This augmentedversion of <strong>z </strong>becomes <u>one </u>basic solution (you have several more, depending on how many candidates for <strong>X </strong>you have in any given case). Following this, you stack all basic solutions into one large matrix <strong>S </strong>and pick <em>rank</em>(<strong>S</strong>)-many columns of <strong>S </strong>(call this matrix <strong>T</strong>; <em>rank</em>(<strong>T</strong>) = <em>rank</em>(<strong>S</strong>)) and present the affine combination of these columns as the general solution to <strong>Ax </strong>= <strong>y</strong>.

The input to your code should be read on command-line through a file. For example, the file input1 on Compass, which is shown in figure 1 presents the relevant details for the instance shown in equation 2 in page 4 of lesson 2 of my notes. The first (second) entry in the file is the number of rows (columns) of <strong>A</strong>. Following this, each element of <strong>A </strong>is a presented in a row-by-row fashion. Finally, the entries of <strong>y </strong>are presented in a row-by-row manner. The format of the input file should be obvious with the example from equation 1 in page 4 of lesson 2 of my notes and what is shown in figure 1 . I am looking for an output along the lines of what is shown in figure 2 for this example. Note that the output in figure 2 says the general solution has the form

<em> .                           </em>(1)

I am also including a file called input2 on Compass that presents the relevant input for the problem in section 3.1 of lesson 2 of my notes. Figure 4 shows the sample output when my C++ code is run on input2. The output in figure 4 says the general solution has the form

 28   37   28                                                                     −7   35<em>γ</em>1 + 44<em>γ</em>2 + 35<em>γ</em>3 − 7 

<sub> </sub>14 <sub> </sub> 14 <sub> </sub> 0 <sub>                                                       </sub> 0 <sub> </sub>                                    14<em>γ</em><sub>1 </sub>+ 14<em>γ</em><sub>2 </sub>

 0   0   −7                                               0                                            −7<em>γ</em>3 

 <em>γ</em>1 15 +<em>γ</em>2 0 +<em>γ</em>3 15 +(1−<em>γ</em>1−<em>γ</em>2−<em>γ</em>3) 15  =          15 − 15<em>γ</em>2 <em>.</em>

 0   −3   0                                               0                                            −3<em>γ</em>2 



 0   0   7                                                0                                              7<em>γ</em><sub>3 </sub>



0                        0                        0                                                 7                           7 − 7<em>γ</em><sub>2 </sub>− 7<em>γ</em><sub>3 </sub>− 7<em>γ</em><sub>1</sub>

(2)

The input file shown in figure 5 describes the equation that is just below equation 2 in page 4 of lesson 2 of my notes. Figure 6 shows the result when my code is run on this input file.

<strong>Some Questions/thoughts…</strong>

<strong>Question</strong>: How do you reconcile the fact that while equation 1 looks similar to the general solution presented in page 7 of lesson 2 of my notes, equation 2 looks different from equation 6 in page 10 of lesson 2.

Figure 1: The format of the input file that describes the problem of equation 2

in page 4 of lesson 2 of my notes.

<strong>References</strong>

Figure 2: Sample output when the file shown in figure 1 is presented as input. The general solution is presented as the affine combination of the two solution vectors shown in the screen.

Figure 3: The format of the input file that describes the problem of section 3.1 of lesson 2 of my notes.

Figure 4: Sample output when the file shown in figure 3 is presented as input. The general solution is presented as the affine combination of the four solution vectors shown in the screen.

Figure 5: The format of the input file that describes the problem just below equation 2 in page 4 of lesson 2 of my notes.

Figure 6: Sample output when the file shown in figure 5 is presented