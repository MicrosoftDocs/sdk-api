---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagGLYPHSET structure


## -description



The <b>GLYPHSET</b> structure contains information about a range of Unicode code points.




## -struct-fields




### -field cbThis

The size, in bytes, of this structure.


### -field flAccel

Flags describing the maximum size of the glyph indices. This member can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>GS_8BIT_INDICES</td>
<td>Treat glyph indices as 8-bit wide values. Otherwise, they are 16-bit wide values.</td>
</tr>
</table>
 


### -field cGlyphsSupported

The total number of Unicode code points supported in the font.


### -field cRanges

The total number of Unicode ranges in <b>ranges</b>.


### -field ranges

Array of Unicode ranges that are supported in the font.


## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/51b0ab12-c467-4a89-8173-fdc513868aae">GetFontUnicodeRanges</a>



<a href="https://msdn.microsoft.com/20959057-6062-4c1e-a23d-535584ba6ea3">WCRANGE</a>
 

 

