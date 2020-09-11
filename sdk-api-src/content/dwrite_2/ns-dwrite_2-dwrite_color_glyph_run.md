---
UID: NS:dwrite_2.DWRITE_COLOR_GLYPH_RUN
title: DWRITE_COLOR_GLYPH_RUN (dwrite_2.h)
description: Contains the information needed by renderers to draw glyph runs with glyph color information.
helpviewer_keywords: ["DWRITE_COLOR_GLYPH_RUN","DWRITE_COLOR_GLYPH_RUN structure [Direct Write]","PDWRITE_COLOR_GLYPH_RUN","PDWRITE_COLOR_GLYPH_RUN structure pointer [Direct Write]","directwrite.dwrite_color_glyph_run","dwrite_2/DWRITE_COLOR_GLYPH_RUN","dwrite_2/PDWRITE_COLOR_GLYPH_RUN"]
old-location: directwrite\dwrite_color_glyph_run.htm
tech.root: DirectWrite
ms.assetid: E70CEE54-80BB-42D2-BBD7-97472AAA4B56
ms.date: 12/05/2018
ms.keywords: DWRITE_COLOR_GLYPH_RUN, DWRITE_COLOR_GLYPH_RUN structure [Direct Write], PDWRITE_COLOR_GLYPH_RUN, PDWRITE_COLOR_GLYPH_RUN structure pointer [Direct Write], directwrite.dwrite_color_glyph_run, dwrite_2/DWRITE_COLOR_GLYPH_RUN, dwrite_2/PDWRITE_COLOR_GLYPH_RUN
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - DWRITE_COLOR_GLYPH_RUN
 - dwrite_2/DWRITE_COLOR_GLYPH_RUN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DWrite_2.h
api_name:
 - DWRITE_COLOR_GLYPH_RUN
---

# DWRITE_COLOR_GLYPH_RUN structure


## -description

Contains the information needed by renderers to draw glyph runs with glyph color information. 
	 All coordinates are in device independent pixels (DIPs).

## -struct-fields

### -field glyphRun

Glyph run to draw for this layer.

### -field glyphRunDescription

Pointer to the glyph run description for this layer. This may be <b>NULL</b>. For example, when the original glyph run is split into multiple layers, one layer might have a description and the others have none.

### -field baselineOriginX

X coordinate of the baseline origin for the layer.

### -field baselineOriginY

Y coordinate of the baseline origin for the layer.

### -field runColor

Color value of the run; if all members are zero, the run should be drawn using the current brush.

### -field paletteIndex

Zero-based index into the font’s color palette; if this is <b>0xFFFF</b>, the run should be drawn using the current brush.

