<PACKAGE "ZSTR">

<ENTRY ZSTR STRING-ZSTR ZSTR-STRING PADCHR>

<NEWTYPE ZSTR BYTES '<BYTES 5>>

<SETG ZCHRS "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ 0123456789.,!?_#'\"/\\|-:()">
<GDECL (ZCHRS) STRING>

<SETG PADCHR 5>
<MANIFEST PADCHR>

<DEFINE ZSTR-STRING (S "AUX" (ZCHRS ,ZCHRS)
			     (CSTEMP 0)
			     (CSPERM 0)
			     (TEMP? <>)
			     (B1 <>))
	#DECL ((VALUE ZCHRS) STRING
	       (S) ZSTR
	       (CSTEMP CSPERM) FIX
	       (TEMP?) <OR ATOM FALSE>
	       (B1) <OR ATOM FIX FALSE>)
	<MAPF ,STRING
	      <FUNCTION (B "AUX" (CS <COND (.TEMP?
					    <SET TEMP? <>>
					    .CSTEMP)
					   (.CSPERM)>))
			#DECL ((VALUE) CHARACTER
			       (B CS) FIX)
			<COND (.B1
			       <COND (<TYPE? .B1 ATOM> <SET B1 .B> <MAPRET>)
				     (<SET B <+ .B <* .B1 32>>>
				      <SET B1 <>>
				      <ASCII .B>)>)
			      (<AND <==? .CS 2> <==? .B 6>>
			       <SET B1 T>
			       <MAPRET>)
			      (<G? .B 5> <NTH .ZCHRS <+ <* .CS 26> .B -5>>)
			      (<0? .B> <ASCII 32>)
			      (<1? .B> <MAPRET <ASCII 13> <ASCII 10>>)
			      (<L? .B 4>
			       <SET TEMP? T>
			       <SET CSTEMP <MOD <+ .CS .B 2> 3>>
			       <MAPRET>)
			      (<SET CSPERM <MOD <+ .CS .B> 3>>
			       <MAPRET>)>>
	      .S>>

<DEFINE ZCHR-CS (C "AUX" RSTR)
	#DECL ((VALUE) FIX
	       (C) CHARACTER
	       (RSTR) <OR STRING FALSE>)
	<COND (<OR <==? .C <ASCII 32>> <==? .C <ASCII 13>>> 3)
	      (<SET RSTR <MEMQ .C ,ZCHRS>>
	       </ <- 78 <LENGTH .RSTR>> 26>)
	      (2)>>

<DEFINE ZCHR-BYTE (C "AUX" RSTR B)
	#DECL ((VALUE) <OR FIX FALSE>
	       (C) CHARACTER
	       (RSTR) <OR STRING FALSE>
	       (B) FIX)
	<AND <SET RSTR <MEMQ .C ,ZCHRS>>
	     <- 6 <- <* </ <SET B <- 78 <LENGTH .RSTR>>> 26> 26> .B>>>>

<DEFINE STRING-ZSTR (S "AUX" (ZCHRS ,ZCHRS) (CS 0) (SKIP? <>))
	#DECL ((VALUE) ZSTR
	       (S ZCHRS) STRING
	       (CS) FIX
	       (SKIP?) <OR ATOM FALSE>)
	<MAPR <FUNCTION ("TUPLE" BTUP)
			#DECL ((VALUE) ZSTR
			       (BTUP) <TUPLE [REST FIX]>)
			<CHTYPE <BYTES 5 !.BTUP> ZSTR>>
	      <FUNCTION (STR "AUX" (C <1 .STR>)
				   (C2 <AND <NOT <EMPTY? <REST .STR>>>
					    <2 .STR>>)
				   NCS
				   PB
				   B)
			#DECL ((VALUE NCS PB) FIX
			       (STR) STRING
			       (C) CHARACTER
			       (C2) <OR CHARACTER FALSE>
			       (B) <OR FIX FALSE>)
			<COND (.SKIP? <SET SKIP? <>> <MAPRET>)
			      (<==? .C <ASCII 32>> 0)
			      (<AND <==? .C <ASCII 13>>
				    .C2
				    <==? .C2 <ASCII 10>>>
			       <SET SKIP? T>
			       1)
			      (<SET PB 0>
			       <COND (<==? <SET NCS <ZCHR-CS .C>> .CS>)
				     (<AND .C2 <==? .NCS <ZCHR-CS .C2>>>
				      <SET PB <+ <MOD <- .NCS .CS> 3> 3>>
				      <SET CS .NCS>)
				     (<SET PB <+ <MOD <- .NCS .CS> 3> 1>>)>
			       <COND (<SET B <ZCHR-BYTE .C>>
				      <OR <0? .PB> <MAPRET .PB .B>>
				      .B)
				     (<SET B <ASCII .C>>
				      <OR <0? .PB>
					  <MAPRET .PB
						  6
						  </ .B 32>
						  <- .B <* </ .B 32> 32>>>>
				      <MAPRET 6
					      </ .B 32>
					      <- .B <* </ .B 32> 32>>>)>)>>
	      .S>>

<DEFINE ZSTR-PRINT (STR)
	#DECL ((STR) ZSTR)
	<PRINC !\">
	<PRINC <ZSTR-STRING .STR>>
	<PRINC !\">>

<PRINTTYPE ZSTR ,ZSTR-PRINT>

<ENDPACKAGE>
