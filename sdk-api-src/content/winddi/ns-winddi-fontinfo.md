---
UID: NS:winddi._FONTINFO
title: FONTINFO (winddi.h)
author: windows-sdk-content
description: The FONTINFO structure contains information regarding a specific font.
old-location: display\fontinfo.htm
tech.root: display
ms.assetid: fdb1539a-f8cb-41fd-bad2-d84c6663b1bb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PFONTINFO, FONTINFO, FONTINFO structure [Display Devices], PFONTINFO, PFONTINFO structure pointer [Display Devices], display.fontinfo, grstrcts_95e2167e-53ae-44d9-a889-be2139bcac99.xml, winddi/FONTINFO, winddi/PFONTINFO"
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - FONTINFO
product: Windows
targetos: Windows
req.typenames: FONTINFO, *PFONTINFO
req.redist: 
ms.custom: 19H1
---

# FONTINFO structure


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



GDI writes and returns this structure through <a href="https://msdn.microsoft.com/4b952bdc-a496-4ded-9390-9f4b470f3a6c">FONTOBJ_vGetInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/4b952bdc-a496-4ded-9390-9f4b470f3a6c">FONTOBJ_vGetInfo</a>
 

 

