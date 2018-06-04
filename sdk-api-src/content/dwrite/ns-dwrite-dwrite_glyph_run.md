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

