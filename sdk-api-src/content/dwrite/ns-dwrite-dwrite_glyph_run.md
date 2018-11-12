---
UID: NS:dwrite.DWRITE_GLYPH_RUN
title: DWRITE_GLYPH_RUN
author: windows-sdk-content
description: Contains the information needed by renderers to draw glyph runs.
old-location: directwrite\dwrite_glyph_run.htm
tech.root: DirectWrite
ms.assetid: 2997d63f-8d33-44c3-9617-cfffe5f61f7d
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DWRITE_GLYPH_RUN, DWRITE_GLYPH_RUN structure [Direct Write], directwrite.dwrite_glyph_run, dwrite/DWRITE_GLYPH_RUN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_GLYPH_RUN
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DWRITE_GLYPH_RUN structure


## -description


Contains the information needed by renderers to draw glyph runs. 
	 All coordinates are in device independent pixels (DIPs).
  


## -struct-fields




### -field fontFace

Type: <b><a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>*</b>

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

Type: <b>const <a href="https://msdn.microsoft.com/f5a231c0-78df-4fe0-99a8-81fcad517cda">DWRITE_GLYPH_OFFSET</a>*</b>

A pointer to an array containing glyph offsets for the glyph run.


### -field isSideways

Type: <b>BOOL</b>

If true, specifies that glyphs are rotated 90 degrees to the left and vertical metrics are used. Vertical writing is achieved by specifying <b>isSideways</b> = true and rotating the entire run 90 degrees to the right via a rotate transform.


### -field bidiLevel

Type: <b>UINT32</b>

The implicit resolved bidi level of the run. Odd levels indicate right-to-left languages like Hebrew and Arabic, while even levels indicate left-to-right languages like English and Japanese (when written horizontally). For right-to-left languages, the text origin is on the right, and text should be drawn to the left.

