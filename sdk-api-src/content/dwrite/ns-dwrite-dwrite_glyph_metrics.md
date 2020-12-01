---
UID: NS:dwrite.DWRITE_GLYPH_METRICS
title: DWRITE_GLYPH_METRICS (dwrite.h)
description: Specifies the metrics of an individual glyph.
helpviewer_keywords: ["DWRITE_GLYPH_METRICS","DWRITE_GLYPH_METRICS structure [Direct Write]","directwrite.dwrite_glyph_metrics","dwrite/DWRITE_GLYPH_METRICS"]
old-location: directwrite\dwrite_glyph_metrics.htm
tech.root: DirectWrite
ms.assetid: d2a4ac9f-f510-4235-93bb-e7bdecc65873
ms.date: 12/05/2018
ms.keywords: DWRITE_GLYPH_METRICS, DWRITE_GLYPH_METRICS structure [Direct Write], directwrite.dwrite_glyph_metrics, dwrite/DWRITE_GLYPH_METRICS
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
 - DWRITE_GLYPH_METRICS
 - dwrite/DWRITE_GLYPH_METRICS
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
 - DWRITE_GLYPH_METRICS
---

# DWRITE_GLYPH_METRICS structure


## -description

Specifies the metrics of an individual glyph.The units depend on how the metrics are obtained.

## -struct-fields

### -field leftSideBearing

Type: <b>INT32</b>

Specifies the X offset from the glyph origin to the left edge of the black box. The glyph origin is the current horizontal writing position. A negative value means the black box extends to the left of the origin (often true for lowercase italic 'f').

### -field advanceWidth

Type: <b>UINT32</b>

Specifies the X offset from the origin of the current glyph to the origin of the next glyph when writing horizontally.

### -field rightSideBearing

Type: <b>INT32</b>

Specifies the X offset from the right edge of the black box to the origin of the next glyph when writing horizontally. The value is negative when the right edge of the black box overhangs the layout box.

### -field topSideBearing

Type: <b>INT32</b>

Specifies the vertical offset from the vertical origin to the top of the black box. Thus, a positive value adds whitespace whereas a negative value means the glyph overhangs the top of the layout box.

### -field advanceHeight

Type: <b>UINT32</b>

Specifies the Y offset from the vertical origin of the current glyph to the vertical origin of the next glyph when writing vertically. Note that the term "origin" by itself denotes the horizontal origin. The vertical origin is different. Its Y coordinate is specified by <b>verticalOriginY</b> value, and its X coordinate is half the <b>advanceWidth</b> to the right of the horizontal origin.

### -field bottomSideBearing

Type: <b>INT32</b>

Specifies the vertical distance from the bottom edge of the black box to the advance height. This is positive when the bottom edge of the black box is within the layout box, or negative when the bottom edge of black box overhangs the layout box.

### -field verticalOriginY

Type: <b>INT32</b>

Specifies the Y coordinate of a glyph's vertical origin, in the font's design coordinate system. The y coordinate of a glyph's vertical origin is the sum of the glyph's top side bearing and the top (that is, yMax) of the glyph's bounding box.

