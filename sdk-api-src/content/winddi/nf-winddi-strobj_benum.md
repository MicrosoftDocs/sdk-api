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

# STROBJ_bEnum function


## -description


The <b>STROBJ_bEnum</b> function enumerates glyph identities and positions.


## -parameters




### -param pstro

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a> structure containing the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566824">GLYPHPOS</a> information.


### -param pc

Pointer to the count, returned by GDI, of GLYPHPOS structures.


### -param ppgpos

Pointer to the array in which GDI writes the GLYPHPOS structures.


## -returns



The return value is <b>TRUE</b> if more glyphs remain to be enumerated, or <b>FALSE</b> if the enumeration is complete. The return value is DDI_ERROR if the glyphs cannot be enumerated, and an error code is logged.




## -remarks



A driver should download only the glyph handles if it caches fonts itself.

The information returned depends on the driver's return value for <a href="https://msdn.microsoft.com/library/windows/hardware/ff556230">DrvGetGlyphMode</a>. 

Bitmaps or outlines can also be obtained from <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structures.

Printer drivers should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff569740">STROBJ_bEnumPositionsOnly</a> instead of <b>STROBJ_bEnum</b> if printer hardware provides internal rendering of TrueType fonts.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556230">DrvGetGlyphMode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565982">FONTOBJ_cGetGlyphs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566824">GLYPHPOS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569740">STROBJ_bEnumPositionsOnly</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569745">STROBJ_vEnumStart</a>
 

 

