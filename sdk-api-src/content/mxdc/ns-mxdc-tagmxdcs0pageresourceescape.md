---
UID: NS:mxdc.tagMxdcS0PageResourceEscape
title: tagMxdcS0PageResourceEscape
author: windows-driver-content
description: The MXDC_S0PAGE_RESOURCE_ESCAPE_T structure is an MXDC_ESCAPE_HEADER_T structure concatenated with an MXDC_XPS_S0PAGE_RESOURCE_T structure.
old-location: gdi\mxdcs0pageresourceescape.htm
old-project: printdocs
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*P_MXDC_S0PAGE_RESOURCE_ESCAPE_T, MXDC_S0PAGE_RESOURCE_ESCAPE_T, MXDC_S0PAGE_RESOURCE_ESCAPE_T structure [Windows GDI], P_MXDC_S0PAGE_RESOURCE_ESCAPE_T, P_MXDC_S0PAGE_RESOURCE_ESCAPE_T structure pointer [Windows GDI], _win32_tagMxdcS0PageResourceEscape_str, gdi.mxdcs0pageresourceescape, mxdc/MXDC_S0PAGE_RESOURCE_ESCAPE_T, mxdc/P_MXDC_S0PAGE_RESOURCE_ESCAPE_T, tagMxdcS0PageResourceEscape"
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
req.typenames: MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mxdc.h
api_name:
-	MXDC_S0PAGE_RESOURCE_ESCAPE_T
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagMxdcS0PageResourceEscape structure


## -description



The <b>MXDC_S0PAGE_RESOURCE_ESCAPE_T</b> structure is an <a href="https://msdn.microsoft.com/3d1f909c-0c3c-49ac-b530-4ce077ad6d94">MXDC_ESCAPE_HEADER_T</a> structure concatenated with an <a href="https://msdn.microsoft.com/af0690a6-3047-4e95-b719-2305948c0f5d">MXDC_XPS_S0PAGE_RESOURCE_T</a> structure.




## -struct-fields




### -field mxdcEscape

An <a href="https://msdn.microsoft.com/3d1f909c-0c3c-49ac-b530-4ce077ad6d94">MXDC_ESCAPE_HEADER_T</a> structure with its <b>opCode</b> member set to MXDCOP_SET_S0PAGE_RESOURCE.


### -field xpsS0PageResourcePassthrough

An <a href="https://msdn.microsoft.com/af0690a6-3047-4e95-b719-2305948c0f5d">MXDC_XPS_S0PAGE_RESOURCE_T</a> structure representing a resource, such as a font or image file, on an XPS document page.


## -remarks



This structure is passed in the <i>lpszInData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function when that function is called with the <a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a> escape, and the <b>opCode</b> member of the <a href="https://msdn.microsoft.com/3d1f909c-0c3c-49ac-b530-4ce077ad6d94">MXDC_ESCAPE_HEADER_T</a> structure is <b>MXDCOP_SET_S0PAGE_RESOURCE</b>. The result is a page resource to send to the MXDC.

Allocate memory for the escape as shown below, set the fields as needed, and then call <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
</pre>
</td>
</tr>
</table></span></div>
The call to <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> must be between a call to <a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a> and a call to <a href="https://msdn.microsoft.com/33e6d005-f00d-4b87-bf7c-fc79c1d05514">EndPage</a>; however, there can be more than one of these calls between the calls to <b>StartPage</b> and <b>EndPage</b>.

Streaming consumption is more efficient if you call <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> with the <b>MXDCOP_SET_S0PAGE_RESOURCE</b> <b>opCode</b> for each resource on the page before you call <b>ExtEscape</b> with the <b>MXDCOP_SET_S0PAGE </b> <b>opCode</b>.




## -see-also




<a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>



<a href="https://msdn.microsoft.com/1e54b151-2324-4d6b-975a-feb42c37b18d">GDI Printer Escape Functions</a>



<a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

