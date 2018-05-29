---
UID: NF:winddi.DrvQueryTrueTypeOutline
title: DrvQueryTrueTypeOutline function
author: windows-sdk-content
description: The DrvQueryTrueTypeOutline function retrieves glyph outlines in native TrueType format.
old-location: display\drvquerytruetypeoutline.htm
old-project: display
ms.assetid: 49123a0c-5096-4a0f-9444-2018b49b2010
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: DrvQueryTrueTypeOutline, DrvQueryTrueTypeOutline function [Display Devices], ddifncs_77215092-0dde-45d4-93f2-11a7b9e69360.xml, display.drvquerytruetypeoutline, winddi/DrvQueryTrueTypeOutline
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	DrvQueryTrueTypeOutline
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvQueryTrueTypeOutline function


## -description


The <b>DrvQueryTrueTypeOutline</b> function retrieves glyph outlines in native TrueType format.


## -parameters




### -param dhpdev

Handle to a physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> structure returned from a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param pfo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure. Details of the font realization can be queried from this structure.


### -param hglyph

Handle to the glyph for which the outline is being queried.


### -param bMetricsOnly

Specifies that font metrics (only) should be returned, or that TrueType outlines should be returned in cubic Bezier format, or that the TrueType outlines should be returned unhinted. This value can be one of the following:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
TTO_METRICS_ONLY

</td>
<td>
Only font metrics are to be returned. Font data (either outlines or bitmaps) will not be returned.

</td>
</tr>
<tr>
<td>
TTO_QUBICS

</td>
<td>
Outlines are to be returned in cubic Bezier format.

</td>
</tr>
<tr>
<td>
TTO_UNHINTED

</td>
<td>
Outlines are to be returned unhinted.

</td>
</tr>
</table>
 


### -param pgldt

Pointer to the buffer where the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566819">GLYPHDATA</a> structure for this glyph should be written. If <i>pgldt</i> is <b>NULL</b>, no data is written to the GLYPHDATA structure.


### -param cjBuf

Specifies the size, in bytes, of the buffer that receives the TrueType outline.


### -param ppoly

Pointer to the buffer where the TrueType outline should be written. The format of the data is in native TrueType format, stored in a TTPOLYGONHEADER structure. See the Microsoft Windows SDK documentation for more information about the TTPOLYGONHEADER structure.


## -returns



The return value is the size, in bytes, required for the <i>ppoly</i> buffer if <i>pgldt</i> is <b>NULL</b>. If <i>pgldt</i> is not <b>NULL</b>, the return value is the number of bytes copied into the <i>ppoly</i> buffer. If an error occurs, the return value is FD_ERROR.




## -remarks



<b>DrvQueryTrueTypeOutline</b> is required for TrueType font drivers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>
 

 

