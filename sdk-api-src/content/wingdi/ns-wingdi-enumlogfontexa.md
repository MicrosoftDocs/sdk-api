---
UID: NS:wingdi.tagENUMLOGFONTEXA
title: ENUMLOGFONTEXA (wingdi.h)
description: The ENUMLOGFONTEX structure contains information about an enumerated font. (ANSI)
helpviewer_keywords: ["*LPENUMLOGFONTEXA","ENUMLOGFONTEX","ENUMLOGFONTEX structure [Windows GDI]","ENUMLOGFONTEXA","ENUMLOGFONTEXW","LPENUMLOGFONTEX","LPENUMLOGFONTEX structure pointer [Windows GDI]","_win32_ENUMLOGFONTEX_str","gdi.enumlogfontex","wingdi/ENUMLOGFONTEX","wingdi/ENUMLOGFONTEXA","wingdi/ENUMLOGFONTEXW","wingdi/LPENUMLOGFONTEX"]
old-location: gdi\enumlogfontex.htm
tech.root: gdi
ms.assetid: 2e848e47-5b5f-46ad-9963-55d6bb6748a9
ms.date: 12/05/2018
ms.keywords: '*LPENUMLOGFONTEXA, ENUMLOGFONTEX, ENUMLOGFONTEX structure [Windows GDI], ENUMLOGFONTEXA, ENUMLOGFONTEXW, LPENUMLOGFONTEX, LPENUMLOGFONTEX structure pointer [Windows GDI], _win32_ENUMLOGFONTEX_str, gdi.enumlogfontex, wingdi/ENUMLOGFONTEX, wingdi/ENUMLOGFONTEXA, wingdi/ENUMLOGFONTEXW, wingdi/LPENUMLOGFONTEX'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ENUMLOGFONTEXW (Unicode) and ENUMLOGFONTEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ENUMLOGFONTEXA, *LPENUMLOGFONTEXA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagENUMLOGFONTEXA
 - wingdi/tagENUMLOGFONTEXA
 - LPENUMLOGFONTEXA
 - wingdi/LPENUMLOGFONTEXA
 - ENUMLOGFONTEXA
 - wingdi/ENUMLOGFONTEXA
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
 - ENUMLOGFONTEX
 - ENUMLOGFONTEXA
 - ENUMLOGFONTEXW
---

# ENUMLOGFONTEXA structure


## -description

The <b>ENUMLOGFONTEX</b> structure contains information about an enumerated font.

## -struct-fields

### -field elfLogFont

A <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that contains values defining the font attributes.

### -field elfFullName

The unique name of the font. For example, ABC Font Company TrueType Bold Italic Sans Serif.

### -field elfStyle

The style of the font. For example, Bold Italic.

### -field elfScript

The script, that is, the character set, of the font. For example, Cyrillic.

## -see-also

<a href="/previous-versions/dd162618(v=vs.85)">EnumFontFamExProc</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>

## -remarks

> [!NOTE]
> The wingdi.h header defines ENUMLOGFONTEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
