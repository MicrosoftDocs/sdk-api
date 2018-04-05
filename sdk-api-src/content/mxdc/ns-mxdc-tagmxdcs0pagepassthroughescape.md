---
UID: NS:mxdc.tagMxdcS0PagePassthroughEscape
title: tagMxdcS0PagePassthroughEscape
author: windows-driver-content
description: The MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T structure is an MXDC_ESCAPE_HEADER_T structure concatenated with an MXDC_S0PAGE_DATA_T structure.
old-location: gdi\mxdcs0pagepassthroughescape.htm
old-project: printdocs
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T structure [Windows GDI], P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T structure pointer [Windows GDI], _win32_tagMxdcS0PagePassthroughEscape_str, gdi.mxdcs0pagepassthroughescape, mxdc/MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, mxdc/P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, tagMxdcS0PagePassthroughEscape"
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
req.typenames: MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mxdc.h
api_name:
-	MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagMxdcS0PagePassthroughEscape structure


## -description



The <b>MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T</b> structure is an <a href="https://msdn.microsoft.com/3d1f909c-0c3c-49ac-b530-4ce077ad6d94">MXDC_ESCAPE_HEADER_T</a> structure concatenated with an <a href="https://msdn.microsoft.com/3dc8e0b9-cf63-4345-93d2-3b60dac42546">MXDC_S0PAGE_DATA_T</a> structure.




## -struct-fields




### -field mxdcEscape

An <a href="https://msdn.microsoft.com/3d1f909c-0c3c-49ac-b530-4ce077ad6d94">MXDC_ESCAPE_HEADER_T</a> structure with its <b>opCode</b> member set to <b>MXDCOP_SET_S0PAGE</b>.


### -field xpsS0PageData

An <a href="https://msdn.microsoft.com/3dc8e0b9-cf63-4345-93d2-3b60dac42546">MxdcS0PageData</a> structure that represents an XPS-document page.


## -remarks



This structure is passed in the <i>lpszInData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function when it is called with the <a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a> escape and the <b>opCode</b> member of the <a href="https://msdn.microsoft.com/3d1f909c-0c3c-49ac-b530-4ce077ad6d94">MXDC_ESCAPE_HEADER_T</a> structure is <b>MXDCOP_SET_S0PAGE</b>. The result is that the Microsoft XML Document Converter (MXDC) passes the page through to the printer without processing it.

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
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
</pre>
</td>
</tr>
</table></span></div>
The call to <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> must be between a call to <a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a> and a call to <a href="https://msdn.microsoft.com/33e6d005-f00d-4b87-bf7c-fc79c1d05514">EndPage</a>.

The calling application is responsible for validating the XML of the XPS document page.

Streaming consumption is more efficient if you call <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>  with <b>MXDCOP_SET_S0PAGE_RESOURCE</b> as <b>opCode</b> for each resource on the page before you call it with <b>MXDCOP_SET_S0PAGE</b>.




## -see-also




<a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>



<a href="https://msdn.microsoft.com/1e54b151-2324-4d6b-975a-feb42c37b18d">GDI Printer Escape Functions</a>



<a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

