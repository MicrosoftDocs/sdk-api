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

# _FD_GLYPHSET structure


## -description


The FD_GLYPHSET structure is used to define the mappings from Unicode characters to glyph handles.


## -struct-fields




### -field cjThis

Specifies the size, in bytes, of the structure, including the array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff570578">WCRUN</a> structures.


### -field flAccel

Specifies accelerator flags. This member must be the following value:

<table>
<tr>
<th>Flags</th>
<th>Meaning</th>
</tr>
<tr>
<td>
GS_8BIT_HANDLES

</td>
<td>
All handles are 8-bit quantities.

</td>
</tr>
<tr>
<td>
GS_16BIT_HANDLES

</td>
<td>
All handles are 16-bit quantities. 

</td>
</tr>
<tr>
<td>
GS_UNICODE_HANDLES

</td>
<td>
For all runs in this structure, the handle is obtained by zero extending the Unicode code point.

</td>
</tr>
</table>
 


### -field cGlyphsSupported

Specifies the total number of glyphs in all runs.


### -field cRuns

Specifies the number of <a href="https://msdn.microsoft.com/library/windows/hardware/ff570578">WCRUN</a> structures in the <b>awcrun</b> array.


### -field awcrun

Is an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff570578">WCRUN</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556266">DrvQueryFontTree</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570578">WCRUN</a>
 

 

