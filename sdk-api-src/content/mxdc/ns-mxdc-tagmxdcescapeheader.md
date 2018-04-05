---
UID: NS:mxdc.tagMxdcEscapeHeader
title: tagMxdcEscapeHeader
author: windows-driver-content
description: The MXDC_ESCAPE_HEADER_T structure holds the operation code for a call to ExtEscape with MXDC_ESCAPE as the nEscape parameter. It also provides the sizes of the input and output buffers.
old-location: gdi\mxdcescapeheader.htm
old-project: printdocs
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*P_MXDC_ESCAPE_HEADER_T, MXDC_ESCAPE_HEADER_T, MXDC_ESCAPE_HEADER_T structure [Windows GDI], P_MXDC_ESCAPE_HEADER_T, P_MXDC_ESCAPE_HEADER_T structure pointer [Windows GDI], _win32_tagMxdcEscapeHeader_str, gdi.mxdcescapeheader, mxdc/MXDC_ESCAPE_HEADER_T, mxdc/P_MXDC_ESCAPE_HEADER_T, tagMxdcEscapeHeader"
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
req.typenames: MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mxdc.h
api_name:
-	MXDC_ESCAPE_HEADER_T
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagMxdcEscapeHeader structure


## -description



The <b>MXDC_ESCAPE_HEADER_T</b> structure holds the operation code for a call to <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> with <a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a> as the <i>nEscape</i> parameter. It also provides the sizes of the input and output buffers.




## -struct-fields




### -field cbInput

The size of the input buffer that will be passed to the <i>lpszOutData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function.


### -field cbOutput

The size of the output buffer. This is the same value as the <i>cbOutput</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function.


### -field opCode

The code constant that tells MXDC what to do.
			 

<table>
<tr>
<th>Operations code</th>
<th>Description</th>
</tr>
<tr>
<td>MXDCOP_GET_FILENAME</td>
<td>Returns, in the <i>lpszOutData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function, either the full path of the output file as a zero-terminated string or the size of that string. See Remarks.</td>
</tr>
<tr>
<td>MXDCOP_PRINTTICKET_FIXED_DOC_SEQ</td>
<td>Associates a print ticket with an XPS fixed document sequence.</td>
</tr>
<tr>
<td>MXDCOP_PRINTTICKET_FIXED_DOC</td>
<td>Associates a print ticket with an XPS document.</td>
</tr>
<tr>
<td>MXDCOP_PRINTTICKET_FIXED_PAGE</td>
<td>Associates a print ticket with an XPS page.</td>
</tr>
<tr>
<td>MXDCOP_SET_S0PAGE</td>
<td>Sends the XPS markup of the current page to the output.</td>
</tr>
<tr>
<td>MXDCOP_SET_S0PAGE_RESOURCE</td>
<td>Sends a resource on the page, such as an image or font, to the output.</td>
</tr>
<tr>
<td>MXDCOP_SET_XPSPASSTHRU_MODE</td>
<td>Puts the MXDC into a pass-through state, enabling an application to write XPS directly to the output file without any processing by the MXDC. An entire document or even document sequence can be written in this way.</td>
</tr>
</table>
 


## -remarks



Before calling <a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a>,_applications should first verify that the driver is MXDC by calling <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> with the <a href="https://msdn.microsoft.com/44054d92-151e-4713-9287-748261a43afd">GETTECHNOLOGY</a> escape. If the driver is the MXDC the function returns the zero-terminated string "http://schemas.microsoft.com/xps/2005/06".

This structure is always at the beginning of the data passed to the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function in its <i>lpszInData</i> parameter.

When <b>opCode</b> is MXDCOP_GET_FILENAME:

<ul>
<li>The <i>lpszInData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function consists of only the <b>MXDC_ESCAPE_HEADER_T</b> structure.</li>
<li>Obtain the output filename by calling <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> twice. <ol>
<li>The first time, pass 4 to the <i>cbOutput</i> parameter of <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>. Set the <i>lpszOutData</i> parameter to point to any allocated 4 bytes of memory. The size of the fully qualified file path will be returned in the <i>lpszOutData</i> parameter of <b>ExtEscape</b>. </li>
<li>Then call the function again. This time set both <i>cbOutput</i> and <i>cbInput</i> to 4+ <i>DataSize</i>. The fully qualified file path will be returned in an <a href="https://msdn.microsoft.com/070bce2e-5055-47e8-9412-2094a636635f">MxdcGetFileNameData</a> structure.</li>
</ol>
</li>
</ul>
When <b>opCode</b> is MXDCOP_PRINTTICKET_FIXED_DOC_SEQ or MXDCOP_PRINTTICKET_FIXED_DOC:

<ul>
<li>The <i>lpszInData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function consists of the <b>MXDC_ESCAPE_HEADER_T</b> structure and an <a href="https://msdn.microsoft.com/d30ba8bb-f429-49d5-963c-b770c3086e97">MxdcPrintTicketPassthrough</a> structure concatenated into an <a href="https://msdn.microsoft.com/79b4f830-3e3f-4c6f-9e61-98e8bf6e2824">MxdcPrintTicketEscape</a> structure.</li>
<li>The call to <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> must occur between a call to <a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a> and a call to <a href="https://msdn.microsoft.com/bf63ea0f-cc73-4943-9c84-52b3b77e141c">EndDoc</a>.</li>
</ul>
When <b>opCode</b> is MXDCOP_PRINTTICKET_FIXED_PAGE:

<ul>
<li>The <i>lpszInData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function consists of the <b>MXDC_ESCAPE_HEADER_T</b> structure and an <a href="https://msdn.microsoft.com/d30ba8bb-f429-49d5-963c-b770c3086e97">MxdcPrintTicketPassthrough</a> structure concatenated into an <a href="https://msdn.microsoft.com/79b4f830-3e3f-4c6f-9e61-98e8bf6e2824">MxdcPrintTicketEscape</a> structure.</li>
<li>The call to <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> must occur between a call to <a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a> and a call to <a href="https://msdn.microsoft.com/33e6d005-f00d-4b87-bf7c-fc79c1d05514">EndPage</a>.</li>
</ul>
When <b>opCode</b> is MXDCOP_SET_S0PAGE:

<ul>
<li>The <i>lpszInData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function consists of the <b>MXDC_ESCAPE_HEADER_T</b> structure and an <a href="https://msdn.microsoft.com/3dc8e0b9-cf63-4345-93d2-3b60dac42546">MxdcS0PageData</a> structure concatenated into an <a href="https://msdn.microsoft.com/949c1ed4-92d5-4c11-a7da-f9d94bafe3f8">MxdcS0PagePassthroughEscape</a> structure.</li>
<li>The call to <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> must occur between a call to <a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a> and a call to <a href="https://msdn.microsoft.com/33e6d005-f00d-4b87-bf7c-fc79c1d05514">EndPage</a>.</li>
<li>The calling application is responsible for validating the XML.</li>
<li>Streaming consumption is more efficient if you call <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> with MXDCOP_SET_S0PAGE_RESOURCE as <b>opCode</b> for each resource on the page before you call it with MXDCOP_SET_S0PAGE.</li>
</ul>
When <b>opCode</b> is MXDCOP_SET_S0PAGE_RESOURCE:

<ul>
<li>The <i>lpszInData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function consists of the <b>MXDC_ESCAPE_HEADER_T</b> structure and an <a href="https://msdn.microsoft.com/af0690a6-3047-4e95-b719-2305948c0f5d">MxdcXpsS0PageResource</a> structure concatenated into an <a href="https://msdn.microsoft.com/e5caa280-f0a5-4a89-b4f1-4f195a537dc6">MxdcS0PageResourceEscape</a> structure.</li>
<li>The call to <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> must occur between a call to <a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a> and a call to <a href="https://msdn.microsoft.com/33e6d005-f00d-4b87-bf7c-fc79c1d05514">EndPage</a>, but there can be multiple such calls between the <b>StartPage</b> and <b>EndPage</b> calls.</li>
<li>Streaming consumption is more efficient if you call <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> with MXDCOP_SET_S0PAGE_RESOURCE as <b>opCode</b> for each resource on the page before you call it with MXDCOP_SET_S0PAGE.</li>
</ul>
When <b>opCode</b> is MXDCOP_SET_XPSPASSTHRU_MODE:

<ul>
<li>The <i>lpszInData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function consists of only the <b>MXDC_ESCAPE_HEADER_T</b> structure.</li>
<li>This call must occur before the call to <a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>



<a href="https://msdn.microsoft.com/1e54b151-2324-4d6b-975a-feb42c37b18d">GDI Printer Escape Functions</a>



<a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

