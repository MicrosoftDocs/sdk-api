---
UID: NS:winddi._GLYPHBITS
title: "_GLYPHBITS"
author: windows-sdk-content
description: The GLYPHBITS structure is used to define a glyph bitmap.
old-location: display\glyphbits.htm
old-project: display
ms.assetid: d7e0b5dd-dd94-4fc2-8c90-0d656a84c46b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GLYPHBITS, GLYPHBITS structure [Display Devices], _GLYPHBITS, display.glyphbits, grstrcts_597a08d2-215a-4bef-8f5b-a90ded3165fc.xml, winddi/GLYPHBITS
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: GLYPHBITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - GLYPHBITS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

