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

# _IFIEXTRA structure


## -description


The IFIEXTRA structure defines additional information for a given typeface that GDI can use. 


## -struct-fields




### -field ulIdentifier

Should be set to zero. This member was used by GDI to identify Type1 fonts on Windows NT 4.0. 


### -field dpFontSig

Specifies the offset in bytes from the beginning of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a> structure to the FONTSIGNATURE structure (described in the Microsoft Window SDK documentation). The driver should set this member to zero if it does not support multiple character sets.

The character set information in FONTSIGNATURE should be consistent with the information provided in the character sets array to which the <b>dpCharSets</b> member of IFIMETRICS points. 


### -field cig

Specifies the number of distinct glyphs in a font that supports glyph indices. The font's glyph handles are contiguous values that range from 0 to (<b>cig</b>-1). For OpenType fonts, this value is stored in the <i>numGlyphs</i> value of the <i>maxp</i> table.

Fonts that do not have contiguous glyph handles should set this member to zero. Note that the Window SDK glyph index APIs will not work for fonts that set this member to zero.


### -field dpDesignVector

Is the offset from the beginning of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a> structure to the DESIGNVECTOR structure for this font. The driver should set <b>dpDesignVector</b> only if this font is a multiple master font. The DESIGNVECTOR structure is described in the Window SDK documentation.


### -field dpAxesInfoW

Is the offset from the beginning of the IFIMETRICS structure to the AXESINFOW structure for this font. The driver should set <b>dpAxesInfoW</b> only if this font is a multiple master font. The AXESINFOW structure is described in the Window SDK documentation.


### -field aulReserved

Is reserved and should be ignored by the driver.


## -remarks



When used, this structure lies below the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a> structure in memory.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556262">DrvQueryFont</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a>
 

 

