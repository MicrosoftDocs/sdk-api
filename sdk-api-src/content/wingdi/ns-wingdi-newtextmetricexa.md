---
UID: NS:wingdi.tagNEWTEXTMETRICEXA
title: NEWTEXTMETRICEXA (wingdi.h)
description: The NEWTEXTMETRICEX structure contains information about a physical font. (ANSI)
helpviewer_keywords: ["NEWTEXTMETRICEX","NEWTEXTMETRICEX structure [Windows GDI]","NEWTEXTMETRICEXA","NEWTEXTMETRICEXW","_win32_NEWTEXTMETRICEX_str","gdi.newtextmetricex","wingdi/NEWTEXTMETRICEX","wingdi/NEWTEXTMETRICEXA","wingdi/NEWTEXTMETRICEXW"]
old-location: gdi\newtextmetricex.htm
tech.root: gdi
ms.assetid: b85ff705-2dd4-4877-9905-d4c2a0894e24
ms.date: 12/05/2018
ms.keywords: NEWTEXTMETRICEX, NEWTEXTMETRICEX structure [Windows GDI], NEWTEXTMETRICEXA, NEWTEXTMETRICEXW, _win32_NEWTEXTMETRICEX_str, gdi.newtextmetricex, wingdi/NEWTEXTMETRICEX, wingdi/NEWTEXTMETRICEXA, wingdi/NEWTEXTMETRICEXW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NEWTEXTMETRICEXW (Unicode) and NEWTEXTMETRICEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NEWTEXTMETRICEXA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNEWTEXTMETRICEXA
 - wingdi/tagNEWTEXTMETRICEXA
 - NEWTEXTMETRICEXA
 - wingdi/NEWTEXTMETRICEXA
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
 - NEWTEXTMETRICEX
 - NEWTEXTMETRICEXA
 - NEWTEXTMETRICEXW
---

# NEWTEXTMETRICEXA structure


## -description

The <b>NEWTEXTMETRICEX</b> structure contains information about a physical font.

## -struct-fields

### -field ntmTm

A <a href="/windows/desktop/api/wingdi/ns-wingdi-newtextmetrica">NEWTEXTMETRIC</a> structure.

### -field ntmFontSig

A <a href="/windows/desktop/api/wingdi/ns-wingdi-fontsignature">FONTSIGNATURE</a> structure indicating the coverage of the font.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-fontsignature">FONTSIGNATURE</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-newtextmetrica">NEWTEXTMETRIC</a>

## -remarks

> [!NOTE]
> The wingdi.h header defines NEWTEXTMETRICEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
