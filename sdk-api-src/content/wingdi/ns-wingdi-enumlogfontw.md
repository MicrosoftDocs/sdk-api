---
UID: NS:wingdi.tagENUMLOGFONTW
title: ENUMLOGFONTW (wingdi.h)
description: The ENUMLOGFONT structure defines the attributes of a font, the complete name of a font, and the style of a font. (Unicode)
helpviewer_keywords: ["*LPENUMLOGFONTW","ENUMLOGFONT","ENUMLOGFONT structure [Windows GDI]","ENUMLOGFONTA","ENUMLOGFONTW","LPENUMLOGFONT","LPENUMLOGFONT structure pointer [Windows GDI]","_win32_ENUMLOGFONT_str","gdi.enumlogfont","wingdi/ENUMLOGFONT","wingdi/ENUMLOGFONTA","wingdi/ENUMLOGFONTW","wingdi/LPENUMLOGFONT"]
old-location: gdi\enumlogfont.htm
tech.root: gdi
ms.assetid: cfae9e97-c714-40fb-88ab-95e12ea3ffa9
ms.date: 12/05/2018
ms.keywords: '*LPENUMLOGFONTW, ENUMLOGFONT, ENUMLOGFONT structure [Windows GDI], ENUMLOGFONTA, ENUMLOGFONTW, LPENUMLOGFONT, LPENUMLOGFONT structure pointer [Windows GDI], _win32_ENUMLOGFONT_str, gdi.enumlogfont, wingdi/ENUMLOGFONT, wingdi/ENUMLOGFONTA, wingdi/ENUMLOGFONTW, wingdi/LPENUMLOGFONT'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ENUMLOGFONTW (Unicode) and ENUMLOGFONTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ENUMLOGFONTW, *LPENUMLOGFONTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagENUMLOGFONTW
 - wingdi/tagENUMLOGFONTW
 - LPENUMLOGFONTW
 - wingdi/LPENUMLOGFONTW
 - ENUMLOGFONTW
 - wingdi/ENUMLOGFONTW
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
 - ENUMLOGFONT
 - ENUMLOGFONTA
 - ENUMLOGFONTW
---

# ENUMLOGFONTW structure


## -description

The <b>ENUMLOGFONT</b> structure defines the attributes of a font, the complete name of a font, and the style of a font.

## -struct-fields

### -field elfLogFont

A <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that defines the attributes of a font.

### -field elfFullName

A unique name for the font. For example, ABCD Font Company TrueType Bold Italic Sans Serif.

### -field elfStyle

The style of the font. For example, Bold Italic.

## -see-also

<a href="/previous-versions/dd162621(v=vs.85)">EnumFontFamProc</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>

## -remarks

> [!NOTE]
> The wingdi.h header defines ENUMLOGFONT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
