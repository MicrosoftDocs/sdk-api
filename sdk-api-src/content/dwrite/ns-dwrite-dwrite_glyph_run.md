---
UID: NS:dwrite.DWRITE_GLYPH_RUN
title: DWRITE_GLYPH_RUN (dwrite.h)
description: Contains the information needed by renderers to draw glyph runs.
helpviewer_keywords: ["DWRITE_GLYPH_RUN","DWRITE_GLYPH_RUN structure [Direct Write]","directwrite.dwrite_glyph_run","dwrite/DWRITE_GLYPH_RUN"]
old-location: directwrite\dwrite_glyph_run.htm
tech.root: DirectWrite
ms.assetid: 2997d63f-8d33-44c3-9617-cfffe5f61f7d
ms.date: 12/05/2018
ms.keywords: DWRITE_GLYPH_RUN, DWRITE_GLYPH_RUN structure [Direct Write], directwrite.dwrite_glyph_run, dwrite/DWRITE_GLYPH_RUN
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_GLYPH_RUN
 - dwrite/DWRITE_GLYPH_RUN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_GLYPH_RUN
---

# DWRITE_GLYPH_RUN structure


## -description

Contains the information needed by renderers to draw glyph runs. 
	 All coordinates are in device independent pixels (DIPs).

## -struct-fields

### -field fontFace

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>*</b>

The physical font face object to draw with.

### -field fontEmSize

Type: <b>FLOAT</b>

The logical size of the font in DIPs (equals 1/96 inch), not points.

### -field glyphCount

Type: <b>UINT32</b>

The number of glyphs in the glyph run.

### -field glyphIndices

Type: <b>const UINT16*</b>

A pointer to an array of indices to render for the glyph run.

### -field glyphAdvances

Type: <b>const FLOAT*</b>

A pointer to an array containing glyph advance widths for the glyph run.

### -field glyphOffsets

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset">DWRITE_GLYPH_OFFSET</a>*</b>

A pointer to an array containing glyph offsets for the glyph run.

### -field isSideways

Type: <b>BOOL</b>

If true, specifies that glyphs are rotated 90 degrees to the left and vertical metrics are used. Vertical writing is achieved by specifying <b>isSideways</b> = true and rotating the entire run 90 degrees to the right via a rotate transform.

### -field bidiLevel

Type: <b>UINT32</b>

The implicit resolved bidi level of the run. Odd levels indicate right-to-left languages like Hebrew and Arabic, while even levels indicate left-to-right languages like English and Japanese (when written horizontally). For right-to-left languages, the text origin is on the right, and text should be drawn to the left.

