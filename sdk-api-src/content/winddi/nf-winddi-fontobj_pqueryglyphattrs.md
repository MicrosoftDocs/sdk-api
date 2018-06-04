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

# FONTOBJ_pQueryGlyphAttrs function


## -description


The <b>FONTOBJ_pQueryGlyphAttrs</b> function returns information about a font's glyphs.


## -parameters




### -param pfo

Is a caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure identifying the font for which attributes are being requested.


### -param iMode [in]

Is a caller-supplied flag indicating the type of glyph attribute being requested. The following flag is defined:

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
FO_ATTR_MODE_ROTATE

</td>
<td>
The function returns an array indicating which glyphs of a vertical font must be rotated.

</td>
</tr>
</table>
 


## -returns



<b>FONTOBJ_pQueryGlyphAttrs</b> returns a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff565623">FD_GLYPHATTR</a> structure. If an error is encountered, such as an invalid input argument, or if the font described by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure is not a vertical font, the function returns <b>NULL</b>.




## -remarks



Currently, the only attribute flag defined is FO_ATTR_MODE_ROTATE. This flag is meant for use by printer drivers that support printers with built-in font rasterizers. The driver can call the <b>FONTOBJ_pQueryGlyphAttrs</b> function, specifying the FO_ATTR_MODE_ROTATE flag, to determine which glyphs within a vertical font must be rotated.

Vertical fonts have a font name that starts with the "@" character. To determine if the current font is a vertical font, the driver can check for the FO_VERT_FACE flag in the <b>flFontType</b> member of the font's <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure.

Rotation information is returned in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565623">FD_GLYPHATTR</a> structure that is used as the function's return value.

The <b>FONTOBJ_pQueryGlyphAttrs</b> function is supplied by GDI. When a printer driver calls <b>FONTOBJ_pQueryGlyphAttrs</b>, GDI calls the appropriate font driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556267">DrvQueryGlyphAttrs</a> function to obtain the requested information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556267">DrvQueryGlyphAttrs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565623">FD_GLYPHATTR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>
 

 

