---
UID: NS:wingdi.tagEXTLOGFONTW
title: EXTLOGFONTW (wingdi.h)
description: The EXTLOGFONT structure defines the attributes of a font. (Unicode)
helpviewer_keywords: ["*LPEXTLOGFONTW","*NPEXTLOGFONTW","*PEXTLOGFONTW","EXTLOGFONT","EXTLOGFONT structure [Windows GDI]","EXTLOGFONTA","EXTLOGFONTW","PEXTLOGFONT","PEXTLOGFONT structure pointer [Windows GDI]","_win32_EXTLOGFONT_str","gdi.extlogfont","wingdi/EXTLOGFONT","wingdi/EXTLOGFONTA","wingdi/EXTLOGFONTW","wingdi/PEXTLOGFONT"]
old-location: gdi\extlogfont.htm
tech.root: gdi
ms.assetid: 19f6364e-3347-45b6-be02-e2cc69a7145a
ms.date: 12/05/2018
ms.keywords: '*LPEXTLOGFONTW, *NPEXTLOGFONTW, *PEXTLOGFONTW, EXTLOGFONT, EXTLOGFONT structure [Windows GDI], EXTLOGFONTA, EXTLOGFONTW, PEXTLOGFONT, PEXTLOGFONT structure pointer [Windows GDI], _win32_EXTLOGFONT_str, gdi.extlogfont, wingdi/EXTLOGFONT, wingdi/EXTLOGFONTA, wingdi/EXTLOGFONTW, wingdi/PEXTLOGFONT'
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
targetos: Windows
req.typenames: EXTLOGFONTW, *PEXTLOGFONTW, *NPEXTLOGFONTW, *LPEXTLOGFONTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEXTLOGFONTW
 - wingdi/tagEXTLOGFONTW
 - PEXTLOGFONTW
 - wingdi/PEXTLOGFONTW
 - EXTLOGFONTW
 - wingdi/EXTLOGFONTW
dev_langs:
 - c++
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
---

# EXTLOGFONTW structure


## -description

The <b>EXTLOGFONT</b> structure defines the attributes of a font.

## -struct-fields

### -field elfLogFont

Specifies some of the attributes of the specified font. This member is a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure.

### -field elfFullName

A unique name for the font (for example, ABCD Font Company TrueType Bold Italic Sans Serif).

### -field elfStyle

The style of the font (for example, Bold Italic).

### -field elfVersion

Reserved. Must be zero.

### -field elfStyleSize

This member only has meaning for hinted fonts. It specifies the point size at which the font is hinted. If set to zero, which is its default value, the font is hinted at the point size corresponding to the <b>lfHeight</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure specified by <b>elfLogFont</b>.

### -field elfMatch

A unique identifier for an enumerated font. This will be filled in by the graphics device interface (GDI) upon font enumeration.

### -field elfReserved

Reserved; must be zero.

### -field elfVendorId

A 4-byte identifier of the font vendor.

### -field elfCulture

Reserved; must be zero.

### -field elfPanose

A <a href="/windows/desktop/api/wingdi/ns-wingdi-panose">PANOSE</a> structure that specifies the shape of the font. If all members of this structure are set to zero, the <b>elfPanose</b> member is ignored by the font mapper.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-panose">PANOSE</a>

## -remarks

> [!NOTE]
> The wingdi.h header defines EXTLOGFONT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
