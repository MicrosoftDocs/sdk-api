---
UID: NS:winddi._GLYPHBITS
title: GLYPHBITS (winddi.h)
description: The GLYPHBITS structure is used to define a glyph bitmap.
helpviewer_keywords: ["GLYPHBITS","GLYPHBITS structure [Display Devices]","display.glyphbits","grstrcts_597a08d2-215a-4bef-8f5b-a90ded3165fc.xml","winddi/GLYPHBITS"]
old-location: display\glyphbits.htm
tech.root: display
ms.assetid: d7e0b5dd-dd94-4fc2-8c90-0d656a84c46b
ms.date: 12/05/2018
ms.keywords: GLYPHBITS, GLYPHBITS structure [Display Devices], display.glyphbits, grstrcts_597a08d2-215a-4bef-8f5b-a90ded3165fc.xml, winddi/GLYPHBITS
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
targetos: Windows
req.typenames: GLYPHBITS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GLYPHBITS
 - winddi/_GLYPHBITS
 - GLYPHBITS
 - winddi/GLYPHBITS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - GLYPHBITS
---

# GLYPHBITS structure


## -description

The GLYPHBITS structure is used to define a glyph bitmap.

## -struct-fields

### -field ptlOrigin

Specifies a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that defines the origin of the character in the bitmap.

### -field sizlBitmap

Specifies a SIZEL structure that contains the width and height, in pixels, of the bitmap. A SIZEL structure is identical to a <a href="/windows/desktop/api/windef/ns-windef-size">SIZE</a> structure.

### -field aj

Is a variable-sized byte array containing a BYTE-aligned bitmap of the glyph. The array must include padding at the end to DWORD-align the entire structure.

GDI will make this request of drivers that have antialiased fonts (see the description of <a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfontcaps">DrvQueryFontCaps</a>). It is possible that a driver may not be able to render a font in a multilevel format. In this case, the driver fails the call and GDI will call the driver again requesting a monochrome realization.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvgetglyphmode">DrvGetGlyphMode</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfontdata">DrvQueryFontData</a>



<a href="/windows/desktop/api/winddi/nf-winddi-fontobj_cgetglyphs">FONTOBJ_cGetGlyphs</a>



<a href="/windows/desktop/api/winddi/ns-winddi-glyphdef">GLYPHDEF</a>