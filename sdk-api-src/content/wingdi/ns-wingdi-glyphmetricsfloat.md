---
UID: NS:wingdi._GLYPHMETRICSFLOAT
title: GLYPHMETRICSFLOAT (wingdi.h)
description: The GLYPHMETRICSFLOAT structure contains information about the placement and orientation of a glyph in a character cell.
helpviewer_keywords: ["*LPGLYPHMETRICSFLOAT","*PGLYPHMETRICSFLOAT","GLYPHMETRICSFLOAT","GLYPHMETRICSFLOAT structure [OpenGL]","PGLYPHMETRICSFLOAT","PGLYPHMETRICSFLOAT structure pointer [OpenGL]","_ogl_GLYPHMETRICSFLOAT","opengl.glyphmetricsfloat","wingdi/GLYPHMETRICSFLOAT","wingdi/PGLYPHMETRICSFLOAT"]
old-location: opengl\glyphmetricsfloat.htm
tech.root: OpenGL
ms.assetid: 6ceccb76-be31-4a4d-b093-1f8e35261a60
ms.date: 12/05/2018
ms.keywords: '*LPGLYPHMETRICSFLOAT, *PGLYPHMETRICSFLOAT, GLYPHMETRICSFLOAT, GLYPHMETRICSFLOAT structure [OpenGL], PGLYPHMETRICSFLOAT, PGLYPHMETRICSFLOAT structure pointer [OpenGL], _ogl_GLYPHMETRICSFLOAT, opengl.glyphmetricsfloat, wingdi/GLYPHMETRICSFLOAT, wingdi/PGLYPHMETRICSFLOAT'
req.header: wingdi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GLYPHMETRICSFLOAT, *PGLYPHMETRICSFLOAT, *LPGLYPHMETRICSFLOAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GLYPHMETRICSFLOAT
 - wingdi/_GLYPHMETRICSFLOAT
 - PGLYPHMETRICSFLOAT
 - wingdi/PGLYPHMETRICSFLOAT
 - GLYPHMETRICSFLOAT
 - wingdi/GLYPHMETRICSFLOAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - GLYPHMETRICSFLOAT
---

# GLYPHMETRICSFLOAT structure


## -description

The <b>GLYPHMETRICSFLOAT</b> structure contains information about the placement and orientation of a glyph in a character cell.

## -struct-fields

### -field gmfBlackBoxX

Specifies the width of the smallest rectangle (the glyph's black box) that completely encloses the glyph.

### -field gmfBlackBoxY

Specifies the height of the smallest rectangle (the glyph's black box) that completely encloses the glyph.

### -field gmfptGlyphOrigin

Specifies the x and y coordinates of the upper-left corner of the smallest rectangle that completely encloses the glyph.

### -field gmfCellIncX

Specifies the horizontal distance from the origin of the current character cell to the origin of the next character cell.

### -field gmfCellIncY

Specifies the vertical distance from the origin of the current character cell to the origin of the next character cell.

## -remarks

The values of <b>GLYPHMETRICSFLOAT</b> are specified as notional units.

## -see-also

<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pointfloat">POINTFLOAT</a>



<a href="/windows/desktop/OpenGL/structures">Structures</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa">wglUseFontOutlines</a>