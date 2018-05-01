---
UID: NS:winddi._FD_GLYPHSET
title: "_FD_GLYPHSET"
author: windows-driver-content
description: The FD_GLYPHSET structure is used to define the mappings from Unicode characters to glyph handles.
old-location: display\fd_glyphset.htm
old-project: display
ms.assetid: af56f2a0-92a6-4217-8121-944a0b4f26f6
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "*PFD_GLYPHSET, FD_GLYPHSET, FD_GLYPHSET structure [Display Devices], PFD_GLYPHSET, PFD_GLYPHSET structure pointer [Display Devices], _FD_GLYPHSET, display.fd_glyphset, grstrcts_69cd5b01-58bb-4141-8f1d-26a6258423ce.xml, winddi/FD_GLYPHSET, winddi/PFD_GLYPHSET"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.typenames: FD_GLYPHSET, *PFD_GLYPHSET
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	FD_GLYPHSET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

