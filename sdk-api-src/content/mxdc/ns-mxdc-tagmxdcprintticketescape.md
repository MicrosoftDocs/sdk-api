---
UID: NS:mxdc.tagMxdcPrintTicketEscape
title: tagMxdcPrintTicketEscape
author: windows-driver-content
description: The MXDC_PRINTTICKET_ESCAPE_T structure is a MXDC_ESCAPE_HEADER_T structure concatenated with a MXDC_PRINTTICKET_DATA_T structure.
old-location: gdi\mxdcprintticketescape.htm
old-project: printdocs
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*P_MXDC_PRINTTICKET_ESCAPE_T, MXDC_PRINTTICKET_ESCAPE_T, MXDC_PRINTTICKET_ESCAPE_T structure [Windows GDI], P_MXDC_PRINTTICKET_ESCAPE_T, P_MXDC_PRINTTICKET_ESCAPE_T structure pointer [Windows GDI], _win32_tagMxdcPrintTicketEscape_str, gdi.mxdcprintticketescape, mxdc/MXDC_PRINTTICKET_ESCAPE_T, mxdc/P_MXDC_PRINTTICKET_ESCAPE_T, tagMxdcPrintTicketEscape"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mxdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mxdc.h
api_name:
-	MXDC_PRINTTICKET_ESCAPE_T
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagMxdcPrintTicketEscape structure


## -description



The <b>MXDC_PRINTTICKET_ESCAPE_T</b> structure is a <a href="https://msdn.microsoft.com/3d1f909c-0c3c-49ac-b530-4ce077ad6d94">MXDC_ESCAPE_HEADER_T</a> structure concatenated with a <a href="https://msdn.microsoft.com/d30ba8bb-f429-49d5-963c-b770c3086e97">MXDC_PRINTTICKET_DATA_T</a> structure.




## -struct-fields




### -field mxdcEscape

A <a href="https://msdn.microsoft.com/3d1f909c-0c3c-49ac-b530-4ce077ad6d94">MXDC_ESCAPE_HEADER_T</a> structure with its <b>opCode</b> member set to MXDCOP_PRINTTICKET_FIXED_PAGE, MXDCOP_PRINTTICKET_FIXED_DOC, or MXDCOP_PRINTTICKET_FIXED_DOC_SEQ.


### -field printTicketData

A <a href="https://msdn.microsoft.com/d30ba8bb-f429-49d5-963c-b770c3086e97">MXDC_PRINTTICKET_DATA_T</a> structure containing the print ticket.


## -remarks



This structure is passed in the <i>lpszInData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function when that function is called with the <a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a> escape and the <b>opCode</b> member of the <a href="https://msdn.microsoft.com/3d1f909c-0c3c-49ac-b530-4ce077ad6d94">MXDC_ESCAPE_HEADER_T</a> structure is <b>MXDCOP_PRINTTICKET_FIXED_PAGE</b>, <b>MXDCOP_PRINTTICKET_FIXED_DOC</b>, or <b>MXDCOP_PRINTTICKET_FIXED_DOC_SEQ</b>. The result is to write the print ticket to the XPS document file.

Allocate memory for the escape as shown below, set the fields as needed, and  then call <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
</pre>
</td>
</tr>
</table></span></div>
If the <b>opCode</b> is set to <b>MXDCOP_PRINTTICKET_FIXED_PAGE</b>, the call to <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> must occur between a call to <a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a> and a call to <a href="https://msdn.microsoft.com/33e6d005-f00d-4b87-bf7c-fc79c1d05514">EndPage</a>. If the <b>opCode</b> set to either <b>MXDCOP_PRINTTICKET_FIXED_DOC</b> or <b>MXDCOP_PRINTTICKET_FIXED_DOC_SEQ</b>, the call to <b>ExtEscape</b> must occur between a call to <a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a> and a call to <a href="https://msdn.microsoft.com/bf63ea0f-cc73-4943-9c84-52b3b77e141c">EndDoc</a>.




## -see-also




<a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>



<a href="https://msdn.microsoft.com/1e54b151-2324-4d6b-975a-feb42c37b18d">GDI Printer Escape Functions</a>



<a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

