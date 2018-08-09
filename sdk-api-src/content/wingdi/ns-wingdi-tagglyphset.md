---
UID: NS:wingdi.tagGLYPHSET
title: tagGLYPHSET
author: windows-sdk-content
description: The GLYPHSET structure contains information about a range of Unicode code points.
old-location: gdi\glyphset.htm
old-project: gdi
ms.assetid: b8ac8d3f-b062-491c-966f-02f3d4c11419
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPGLYPHSET, *PGLYPHSET, GLYPHSET, GLYPHSET structure [Windows GDI], PGLYPHSET, PGLYPHSET structure pointer [Windows GDI], _win32_GLYPHSET_str, gdi.glyphset, tagGLYPHSET, wingdi/GLYPHSET, wingdi/PGLYPHSET"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GLYPHSET, *PGLYPHSET, *LPGLYPHSET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - GLYPHSET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

