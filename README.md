Download Link: https://assignmentchef.com/product/solved-csci301-assignment2-hexadecimal-numbers
<br>



[<strong>Q1-3</strong>] Fill out the following Assignment2.JSON file. The values in the file must be <strong>represented as hexadecimal numbers</strong>. For example, the hexadecimal representation of decimal number 10 is 0xA.

<table width="542">

 <tbody>

  <tr>

   <td width="542">{“DSAParam”: [&lt;g&gt;, &lt;p&gt;, &lt;q&gt;],“pubkey”: &lt;pubKey&gt;,“Sig”: &lt;sig&gt;,“pubKeyHash”: &lt;pubKeyHash&gt; }</td>

  </tr>

 </tbody>

</table>

<em>Assignment2.JSON </em>




<strong>Q1</strong>.  Create your own public key (i.e., verification key) and private key (i.e, signing key) pair for DSA 2048 bit digital signature using <strong>Pycryptodome.</strong> Write the DSA public parameters, &lt;g&gt;,&lt;p&gt; and &lt;q&gt;, and the public key &lt;pubKey&gt; in <em>Assignment2.JSON</em>.




<strong>Q2.</strong>  Compute a signature by digitally signing “CSCI301 Contemporary topic in security” using your key generated in Q1. For signing, use DSA 2048 bit and SHA256 using the DSS class in <strong>Pycryptodome</strong> with “fips-186-3” option. Write the signature to &lt;sig&gt; in <em>Assignment2.JSON</em>.




<strong>Q3. </strong> To compute  &lt;pubKeyHash&gt;, firstly, compute the hash value of your public key using SHA256 and, then, take the 160 least significant bits of the hash value. Write the result to &lt;pubKeyHash&gt; in <em>Assignment2.JSON</em>.




<strong>Q4</strong>.  Using the completed Assignment2.JSON file, execute the following <strong>“Pay-to-Pubkey-Hash”</strong> script and show each step of script processing by printing out the values in the stack.

<em>&lt;sig&gt; &lt;pubKey&gt; OP_DUP OP_HASH160 </em><em>&lt;pubKeyHash&gt; OP_EQUALVERIFY </em>

<em>OP_CHECKSIG </em>

thout permission from

Jongkil Kim

To make the script work with the values written in <em>Assignment2.JSON</em>. The cryptographic algorithms used in OP_HASH160 and OP_CHECKSIG are redefined as follows:

<em>OP_HASH160</em>: This operator computes the 160 least significant bits of SHA256 hash value of the last value in the stack.

<em>OP_CHECKSIG</em>: This operator verifies a signature &lt;A&gt; with the message “CSCI301 Contemporary topic in security” using a public key &lt;B&gt; when the last two values in the stack are &lt;A&gt; &lt;B&gt;. For the verification, DSA 2048bits with SHA256 is used in a way defined DSS (fips-186-3).

<strong> </strong>

<strong>Q5</strong>. [15 marks] <strong>A report </strong>that 1) gives all necessary information to run your programs (e.g., the other python packages for your code, if they are used) and 2) explain expected outcomes (with screenshots) of each program.