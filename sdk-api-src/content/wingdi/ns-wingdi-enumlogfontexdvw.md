---
UID: NS:wingdi.tagENUMLOGFONTEXDVW
title: ENUMLOGFONTEXDVW (wingdi.h)
description: The ENUMLOGFONTEXDV structure contains the information used to create a font. (Unicode)
helpviewer_keywords: ["*LPENUMLOGFONTEXDVW","*PENUMLOGFONTEXDVW","ENUMLOGFONTEXDV","ENUMLOGFONTEXDV structure [Windows GDI]","ENUMLOGFONTEXDVA","ENUMLOGFONTEXDVW","PENUMLOGFONTEXDV","PENUMLOGFONTEXDV structure pointer [Windows GDI]","_win32_ENUMLOGFONTEXDV_str","gdi.enumlogfontexdv","wingdi/ENUMLOGFONTEXDV","wingdi/ENUMLOGFONTEXDVA","wingdi/ENUMLOGFONTEXDVW","wingdi/PENUMLOGFONTEXDV"]
old-location: gdi\enumlogfontexdv.htm
tech.root: gdi
ms.assetid: 8d483f52-250e-4c4f-83cf-ff952bb84fd3
ms.date: 12/05/2018
ms.keywords: '*LPENUMLOGFONTEXDVW, *PENUMLOGFONTEXDVW, ENUMLOGFONTEXDV, ENUMLOGFONTEXDV structure [Windows GDI], ENUMLOGFONTEXDVA, ENUMLOGFONTEXDVW, PENUMLOGFONTEXDV, PENUMLOGFONTEXDV structure pointer [Windows GDI], _win32_ENUMLOGFONTEXDV_str, gdi.enumlogfontexdv, wingdi/ENUMLOGFONTEXDV, wingdi/ENUMLOGFONTEXDVA, wingdi/ENUMLOGFONTEXDVW, wingdi/PENUMLOGFONTEXDV'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ENUMLOGFONTEXDVW (Unicode) and ENUMLOGFONTEXDVA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ENUMLOGFONTEXDVW, *PENUMLOGFONTEXDVW, *LPENUMLOGFONTEXDVW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagENUMLOGFONTEXDVW
 - wingdi/tagENUMLOGFONTEXDVW
 - PENUMLOGFONTEXDVW
 - wingdi/PENUMLOGFONTEXDVW
 - ENUMLOGFONTEXDVW
 - wingdi/ENUMLOGFONTEXDVW
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
 - ENUMLOGFONTEXDV
 - ENUMLOGFONTEXDVA
 - ENUMLOGFONTEXDVW
---

# ENUMLOGFONTEXDVW structure


## -description

The <b>ENUMLOGFONTEXDV</b> structure contains the information used to create a font.

## -struct-fields

### -field elfEnumLogfontEx

An <a href="/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexa">ENUMLOGFONTEX</a> structure that contains information about the logical attributes of the font.

### -field elfDesignVector

A <a href="/windows/desktop/api/wingdi/ns-wingdi-designvector">DESIGNVECTOR</a> structure. This is zero-filled unless the font described is a multiple master OpenType font.

## -remarks

The actual size of <b>ENUMLOGFONTEXDV</b> depends on that of <a href="/windows/desktop/api/wingdi/ns-wingdi-designvector">DESIGNVECTOR</a>, which, in turn depends on its <b>dvNumAxes</b> member.

The <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> functions have been modified to return pointers to <a href="/windows/desktop/api/wingdi/ns-wingdi-enumtextmetrica">ENUMTEXTMETRIC</a> and <b>ENUMLOGFONTEXDV</b> to the callback function.





> [!NOTE]
> The wingdi.h header defines ENUMLOGFONTEXDV as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirectexa">CreateFontIndirectEx</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-designvector">DESIGNVECTOR</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-enumtextmetrica">ENUMTEXTMETRIC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>
