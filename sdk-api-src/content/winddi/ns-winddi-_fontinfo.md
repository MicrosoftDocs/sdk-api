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

# _FONTINFO structure


## -description


The FONTINFO structure contains information regarding a specific font. 


## -struct-fields




### -field cjThis

Specifies the size of this FONTINFO structure in bytes.


### -field flCaps

Is a set of capabilities flags. The allowed flags are FO_DEVICE_FONT and FO_OUTLINE_CAPABLE.


### -field cGlyphsSupported

Specifies the number of glyphs in the font.


### -field cjMaxGlyph1

Specifies the size of the largest glyph in 1 bit/pixel. A nonzero value implies that 1-bit-per-pixel bitmaps are supported.


### -field cjMaxGlyph4

Specifies the size of the largest glyph in 4 bits/pixel. A nonzero value implies that 4-bit-per-pixel bitmaps are supported.


### -field cjMaxGlyph8

Specifies the size of the largest glyph in 8 bits/pixel. A nonzero value implies that 8-bit-per-pixel bitmaps are supported.


### -field cjMaxGlyph32

Specifies the size of the largest glyph in 32 bits/pixel. A nonzero value implies that 32-bit-per-pixel bitmaps are supported.


## -remarks



GDI writes and returns this structure through <a href="https://msdn.microsoft.com/library/windows/hardware/ff566013">FONTOBJ_vGetInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff566013">FONTOBJ_vGetInfo</a>
 

 

