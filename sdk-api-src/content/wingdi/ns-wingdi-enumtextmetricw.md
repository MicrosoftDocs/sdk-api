---
UID: NS:wingdi.tagENUMTEXTMETRICW
title: ENUMTEXTMETRICW (wingdi.h)
description: The ENUMTEXTMETRIC structure contains information about a physical font. (Unicode)
helpviewer_keywords: ["*LPENUMTEXTMETRICW","*PENUMTEXTMETRICW","ENUMTEXTMETRIC","ENUMTEXTMETRIC structure [Windows GDI]","ENUMTEXTMETRICA","ENUMTEXTMETRICW","PENUMTEXTMETRIC","PENUMTEXTMETRIC structure pointer [Windows GDI]","_win32_ENUMTEXTMETRIC_str","gdi.enumtextmetric","wingdi/ENUMTEXTMETRIC","wingdi/ENUMTEXTMETRICA","wingdi/ENUMTEXTMETRICW","wingdi/PENUMTEXTMETRIC"]
old-location: gdi\enumtextmetric.htm
tech.root: gdi
ms.assetid: deb81846-3ada-4c88-8c26-74224538d282
ms.date: 12/05/2018
ms.keywords: '*LPENUMTEXTMETRICW, *PENUMTEXTMETRICW, ENUMTEXTMETRIC, ENUMTEXTMETRIC structure [Windows GDI], ENUMTEXTMETRICA, ENUMTEXTMETRICW, PENUMTEXTMETRIC, PENUMTEXTMETRIC structure pointer [Windows GDI], _win32_ENUMTEXTMETRIC_str, gdi.enumtextmetric, wingdi/ENUMTEXTMETRIC, wingdi/ENUMTEXTMETRICA, wingdi/ENUMTEXTMETRICW, wingdi/PENUMTEXTMETRIC'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ENUMTEXTMETRICW (Unicode) and ENUMTEXTMETRICA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ENUMTEXTMETRICW, *PENUMTEXTMETRICW, *LPENUMTEXTMETRICW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagENUMTEXTMETRICW
 - wingdi/tagENUMTEXTMETRICW
 - PENUMTEXTMETRICW
 - wingdi/PENUMTEXTMETRICW
 - ENUMTEXTMETRICW
 - wingdi/ENUMTEXTMETRICW
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
 - ENUMTEXTMETRIC
 - ENUMTEXTMETRICA
 - ENUMTEXTMETRICW
---

# ENUMTEXTMETRICW structure


## -description

The <b>ENUMTEXTMETRIC</b> structure contains information about a physical font.

## -struct-fields

### -field etmNewTextMetricEx

A <a href="/windows/desktop/api/wingdi/ns-wingdi-newtextmetricexa">NEWTEXTMETRICEX</a> structure, containing information about a physical font.

### -field etmAxesList

An <a href="/windows/desktop/api/wingdi/ns-wingdi-axeslista">AXESLIST</a> structure, containing information about the axes for the font. This is only used for multiple master fonts.

## -remarks

<b>ENUMTEXTMETRIC</b> is an extension of <a href="/windows/desktop/api/wingdi/ns-wingdi-newtextmetricexa">NEWTEXTMETRICEX</a> that includes the axis information for a multiple master font.

The <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> functions have been modified to return pointers to the <b>ENUMTEXTMETRIC</b> and <a href="/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexdva">ENUMLOGFONTEXDV</a> structures.





> [!NOTE]
> The wingdi.h header defines ENUMTEXTMETRIC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-axeslista">AXESLIST</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexa">ENUMLOGFONTEX</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexdva">ENUMLOGFONTEXDV</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-enumtextmetrica">ENUMTEXTMETRIC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-newtextmetricexa">NEWTEXTMETRICEX</a>
