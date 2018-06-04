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

