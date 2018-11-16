---
UID: NS:winddi._GLYPHBITS
title: "_GLYPHBITS"
author: windows-sdk-content
description: The GLYPHBITS structure is used to define a glyph bitmap.
old-location: display\glyphbits.htm
tech.root: display
ms.assetid: d7e0b5dd-dd94-4fc2-8c90-0d656a84c46b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GLYPHBITS, GLYPHBITS structure [Display Devices], _GLYPHBITS, display.glyphbits, grstrcts_597a08d2-215a-4bef-8f5b-a90ded3165fc.xml, winddi/GLYPHBITS
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: GLYPHBITS
req.redist: 
---

# _GLYPHBITS structure


## -description


The GLYPHBITS structure is used to define a glyph bitmap.


## -struct-fields




### -field ptlOrigin

Specifies a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that defines the origin of the character in the bitmap.


### -field sizlBitmap

Specifies a SIZEL structure that contains the width and height, in pixels, of the bitmap. A SIZEL structure is identical to a <a href="https://msdn.microsoft.com/08d81096-069f-4554-9bb9-d4a37c0950ac">SIZE</a> structure.


### -field aj

Is a variable-sized byte array containing a BYTE-aligned bitmap of the glyph. The array must include padding at the end to DWORD-align the entire structure.

GDI will make this request of drivers that have antialiased fonts (see the description of <a href="https://msdn.microsoft.com/304ee95a-7e40-40cb-a66c-17397dac0a76">DrvQueryFontCaps</a>). It is possible that a driver may not be able to render a font in a multilevel format. In this case, the driver fails the call and GDI will call the driver again requesting a monochrome realization.


## -see-also




<a href="https://msdn.microsoft.com/8e11c4e7-0203-4445-8f33-3b928161c62a">DrvGetGlyphMode</a>



<a href="https://msdn.microsoft.com/3f6efd3c-3ddf-4ce6-9527-730e01c45e74">DrvQueryFontData</a>



<a href="https://msdn.microsoft.com/0174fc88-e665-427e-b22f-468ddbea5b47">FONTOBJ_cGetGlyphs</a>



<a href="https://msdn.microsoft.com/d1a7a02c-acaf-46b5-9ffe-fddbb01408a5">GLYPHDEF</a>
 

 

