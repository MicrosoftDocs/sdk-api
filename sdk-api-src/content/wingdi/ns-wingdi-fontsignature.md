---
UID: NS:wingdi.tagFONTSIGNATURE
title: FONTSIGNATURE (wingdi.h)
description: Contains information identifying the code pages and Unicode subranges for which a given font provides glyphs.
helpviewer_keywords: ["*LPFONTSIGNATURE","*PFONTSIGNATURE","FONTSIGNATURE","FONTSIGNATURE structure [Internationalization for Windows Applications]","PFONTSIGNATURE","PFONTSIGNATURE structure pointer [Internationalization for Windows Applications]","_win32_FONTSIGNATURE_str","intl.fontsignature","wingdi/FONTSIGNATURE","wingdi/PFONTSIGNATURE"]
old-location: intl\fontsignature.htm
tech.root: Intl
ms.assetid: 5331da53-7e3d-46e9-a922-da04fedc8382
ms.date: 12/05/2018
ms.keywords: '*LPFONTSIGNATURE, *PFONTSIGNATURE, FONTSIGNATURE, FONTSIGNATURE structure [Internationalization for Windows Applications], PFONTSIGNATURE, PFONTSIGNATURE structure pointer [Internationalization for Windows Applications], _win32_FONTSIGNATURE_str, intl.fontsignature, wingdi/FONTSIGNATURE, wingdi/PFONTSIGNATURE'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: FONTSIGNATURE, *PFONTSIGNATURE, *LPFONTSIGNATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFONTSIGNATURE
 - wingdi/tagFONTSIGNATURE
 - PFONTSIGNATURE
 - wingdi/PFONTSIGNATURE
 - FONTSIGNATURE
 - wingdi/FONTSIGNATURE
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
 - FONTSIGNATURE
---

# FONTSIGNATURE structure


## -description

Contains information identifying the code pages and Unicode subranges for which a given font provides glyphs.

## -struct-fields

### -field fsUsb

A 128-bit Unicode subset bitfield (USB) identifying up to 126 Unicode subranges. Each bit, except the two most significant bits, represents a single subrange. The most significant bit is always 1 and identifies the bitfield as a font signature; the second most significant bit is reserved and must be 0. Unicode subranges are numbered in accordance with the ISO 10646 standard. For more information, see <a href="/windows/desktop/Intl/unicode-subset-bitfields">Unicode Subset Bitfields</a>.

### -field fsCsb

A 64-bit, code-page bitfield (CPB) that identifies a specific character set or code page. Code pages are in the lower 32 bits of this bitfield. The high 32 are used for non-Windows code pages. For more information, see <a href="/windows/desktop/Intl/code-page-bitfields">Code Page Bitfields</a>.

## -remarks

GDI relies on Windows code pages fitting within a 32-bit value. Furthermore, the highest 2 bits within this value are reserved for GDI internal use and may not be assigned to code pages.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-localesignature">LOCALESIGNATURE</a>



<a href="/windows/desktop/Intl/unicode-and-character-set-structures">Unicode and Character Set Structures</a>