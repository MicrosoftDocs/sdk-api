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

# DWRITE_GLYPH_METRICS structure


## -description


Specifies the metrics of an individual glyph.
	  The units depend on how the metrics are obtained.


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

