---
UID: NS:wingdi.tagEXTLOGFONTA
title: EXTLOGFONTA (wingdi.h)
description: The EXTLOGFONT structure defines the attributes of a font.helpviewer_keywords: ["*LPEXTLOGFONTA","*NPEXTLOGFONTA","*PEXTLOGFONTA","EXTLOGFONT","EXTLOGFONT structure [Windows GDI]","EXTLOGFONTA","EXTLOGFONTW","PEXTLOGFONT","PEXTLOGFONT structure pointer [Windows GDI]","_win32_EXTLOGFONT_str","gdi.extlogfont","wingdi/EXTLOGFONT","wingdi/EXTLOGFONTA","wingdi/EXTLOGFONTW","wingdi/PEXTLOGFONT"]
old-location: gdi\extlogfont.htm
tech.root: gdi
ms.assetid: 19f6364e-3347-45b6-be02-e2cc69a7145a
ms.date: 12/05/2018
ms.keywords: '*LPEXTLOGFONTA, *NPEXTLOGFONTA, *PEXTLOGFONTA, EXTLOGFONT, EXTLOGFONT structure [Windows GDI], EXTLOGFONTA, EXTLOGFONTW, PEXTLOGFONT, PEXTLOGFONT structure pointer [Windows GDI], _win32_EXTLOGFONT_str, gdi.extlogfont, wingdi/EXTLOGFONT, wingdi/EXTLOGFONTA, wingdi/EXTLOGFONTW, wingdi/PEXTLOGFONT'
f1_keywords:
- wingdi/EXTLOGFONT
dev_langs:
- c++
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EXTLOGFONTW (Unicode) and EXTLOGFONTA (ANSI)
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
- Wingdi.h
api_name:
- EXTLOGFONT
- EXTLOGFONTA
- EXTLOGFONTW
targetos: Windows
req.typenames: EXTLOGFONTA, *PEXTLOGFONTA, *NPEXTLOGFONTA, *LPEXTLOGFONTA
req.redist: 
ms.custom: 19H1
---

# EXTLOGFONTA structure


## -description



The <b>EXTLOGFONT</b> structure defines the attributes of a font.




## -struct-fields




### -field elfLogFont

Specifies some of the attributes of the specified font. This member is a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure.


### -field elfFullName

A unique name for the font (for example, ABCD Font Company TrueType Bold Italic Sans Serif).


### -field elfStyle

The style of the font (for example, Bold Italic).


### -field elfVersion

Reserved. Must be zero.


### -field elfStyleSize

This member only has meaning for hinted fonts. It specifies the point size at which the font is hinted. If set to zero, which is its default value, the font is hinted at the point size corresponding to the <b>lfHeight</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure specified by <b>elfLogFont</b>.


### -field elfMatch

A unique identifier for an enumerated font. This will be filled in by the graphics device interface (GDI) upon font enumeration.


### -field elfReserved

Reserved; must be zero.


### -field elfVendorId

A 4-byte identifier of the font vendor.


### -field elfCulture

Reserved; must be zero.


### -field elfPanose

A <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-panose">PANOSE</a> structure that specifies the shape of the font. If all members of this structure are set to zero, the <b>elfPanose</b> member is ignored by the font mapper.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-panose">PANOSE</a>
 

 

