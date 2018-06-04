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

# _GLYPHBITS structure


## -description


The GLYPHBITS structure is used to define a glyph bitmap.


## -struct-fields




### -field ptlOrigin

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that defines the origin of the character in the bitmap.


### -field sizlBitmap

Specifies a SIZEL structure that contains the width and height, in pixels, of the bitmap. A SIZEL structure is identical to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure.


### -field aj

Is a variable-sized byte array containing a BYTE-aligned bitmap of the glyph. The array must include padding at the end to DWORD-align the entire structure.

GDI will make this request of drivers that have antialiased fonts (see the description of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556263">DrvQueryFontCaps</a>). It is possible that a driver may not be able to render a font in a multilevel format. In this case, the driver fails the call and GDI will call the driver again requesting a monochrome realization.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556230">DrvGetGlyphMode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556264">DrvQueryFontData</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565982">FONTOBJ_cGetGlyphs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566822">GLYPHDEF</a>
 

 

