---
UID: NS:wingdi._GLYPHMETRICS
title: GLYPHMETRICS (wingdi.h)
description: The GLYPHMETRICS structure contains information about the placement and orientation of a glyph in a character cell.
helpviewer_keywords: ["*LPGLYPHMETRICS","GLYPHMETRICS","GLYPHMETRICS structure [Windows GDI]","LPGLYPHMETRICS","LPGLYPHMETRICS structure pointer [Windows GDI]","_win32_GLYPHMETRICS_str","gdi.glyphmetrics","wingdi/GLYPHMETRICS","wingdi/LPGLYPHMETRICS"]
old-location: gdi\glyphmetrics.htm
tech.root: gdi
ms.assetid: a6fa3813-56f7-4b54-b21d-8aabc2309a34
ms.date: 12/05/2018
ms.keywords: '*LPGLYPHMETRICS, GLYPHMETRICS, GLYPHMETRICS structure [Windows GDI], LPGLYPHMETRICS, LPGLYPHMETRICS structure pointer [Windows GDI], _win32_GLYPHMETRICS_str, gdi.glyphmetrics, wingdi/GLYPHMETRICS, wingdi/LPGLYPHMETRICS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GLYPHMETRICS, *LPGLYPHMETRICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GLYPHMETRICS
 - wingdi/_GLYPHMETRICS
 - LPGLYPHMETRICS
 - wingdi/LPGLYPHMETRICS
 - GLYPHMETRICS
 - wingdi/GLYPHMETRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - GLYPHMETRICS
---

# GLYPHMETRICS structure


## -description

The <b>GLYPHMETRICS</b> structure contains information about the placement and orientation of a glyph in a character cell.

## -struct-fields

### -field gmBlackBoxX

The width of the smallest rectangle that completely encloses the glyph (its black box).

### -field gmBlackBoxY

The height of the smallest rectangle that completely encloses the glyph (its black box).

### -field gmptGlyphOrigin

The x- and y-coordinates of the upper left corner of the smallest rectangle that completely encloses the glyph.

### -field gmCellIncX

The horizontal distance from the origin of the current character cell to the origin of the next character cell.

### -field gmCellIncY

The vertical distance from the origin of the current character cell to the origin of the next character cell.

## -remarks

Values in the <b>GLYPHMETRICS</b> structure are specified in device units.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getglyphoutlinea">GetGlyphOutline</a>