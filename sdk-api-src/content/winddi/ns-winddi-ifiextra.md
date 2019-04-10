---
UID: NS:winddi._IFIEXTRA
title: IFIEXTRA (winddi.h)
author: windows-sdk-content
description: The IFIEXTRA structure defines additional information for a given typeface that GDI can use.
old-location: display\ifiextra.htm
tech.root: display
ms.assetid: acca1291-9f58-4520-a4ec-52dc9062630b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PIFIEXTRA, IFIEXTRA, IFIEXTRA structure [Display Devices], PIFIEXTRA, PIFIEXTRA structure pointer [Display Devices], display.ifiextra, grstrcts_6e899cbd-3ebb-4f19-8d04-3e0ca9215fea.xml, winddi/IFIEXTRA, winddi/PIFIEXTRA"
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
 - IFIEXTRA
product: Windows
targetos: Windows
req.typenames: IFIEXTRA, *PIFIEXTRA
req.redist: 
---

# IFIEXTRA structure


## -description


The IFIEXTRA structure defines additional information for a given typeface that GDI can use. 


## -struct-fields




### -field ulIdentifier

Should be set to zero. This member was used by GDI to identify Type1 fonts on Windows NT 4.0. 


### -field dpFontSig

Specifies the offset in bytes from the beginning of the <a href="https://msdn.microsoft.com/fd2606ed-ec61-430a-aaad-38a4c3a207b6">IFIMETRICS</a> structure to the FONTSIGNATURE structure (described in the Microsoft Window SDK documentation). The driver should set this member to zero if it does not support multiple character sets.

The character set information in FONTSIGNATURE should be consistent with the information provided in the character sets array to which the <b>dpCharSets</b> member of IFIMETRICS points. 


### -field cig

Specifies the number of distinct glyphs in a font that supports glyph indices. The font's glyph handles are contiguous values that range from 0 to (<b>cig</b>-1). For OpenType fonts, this value is stored in the <i>numGlyphs</i> value of the <i>maxp</i> table.

Fonts that do not have contiguous glyph handles should set this member to zero. Note that the Window SDK glyph index APIs will not work for fonts that set this member to zero.


### -field dpDesignVector

Is the offset from the beginning of the <a href="https://msdn.microsoft.com/fd2606ed-ec61-430a-aaad-38a4c3a207b6">IFIMETRICS</a> structure to the DESIGNVECTOR structure for this font. The driver should set <b>dpDesignVector</b> only if this font is a multiple master font. The DESIGNVECTOR structure is described in the Window SDK documentation.


### -field dpAxesInfoW

Is the offset from the beginning of the IFIMETRICS structure to the AXESINFOW structure for this font. The driver should set <b>dpAxesInfoW</b> only if this font is a multiple master font. The AXESINFOW structure is described in the Window SDK documentation.


### -field aulReserved

Is reserved and should be ignored by the driver.


## -remarks



When used, this structure lies below the <a href="https://msdn.microsoft.com/fd2606ed-ec61-430a-aaad-38a4c3a207b6">IFIMETRICS</a> structure in memory.




## -see-also




<a href="https://msdn.microsoft.com/2ba6c8e3-9707-48dd-98d9-072f3eee8cd0">DrvQueryFont</a>



<a href="https://msdn.microsoft.com/fd2606ed-ec61-430a-aaad-38a4c3a207b6">IFIMETRICS</a>
 

 

