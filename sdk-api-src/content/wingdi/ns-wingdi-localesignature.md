---
UID: NS:wingdi.tagLOCALESIGNATURE
title: LOCALESIGNATURE (wingdi.h)
description: Contains extended font signature information, including two code page bitfields (CPBs) that define the default and supported character sets and code pages. This structure is typically used to represent the relationships between font coverage and locales.
helpviewer_keywords: ["*LPLOCALESIGNATURE","*PLOCALESIGNATURE","LOCALESIGNATURE","LOCALESIGNATURE structure [Internationalization for Windows Applications]","PLOCALESIGNATURE","PLOCALESIGNATURE structure pointer [Internationalization for Windows Applications]","_win32_LOCALESIGNATURE_str","intl.localesignature","wingdi/LOCALESIGNATURE","wingdi/PLOCALESIGNATURE"]
old-location: intl\localesignature.htm
tech.root: Intl
ms.assetid: 54510d73-f2a2-4176-8080-cdf855e99217
ms.date: 12/05/2018
ms.keywords: '*LPLOCALESIGNATURE, *PLOCALESIGNATURE, LOCALESIGNATURE, LOCALESIGNATURE structure [Internationalization for Windows Applications], PLOCALESIGNATURE, PLOCALESIGNATURE structure pointer [Internationalization for Windows Applications], _win32_LOCALESIGNATURE_str, intl.localesignature, wingdi/LOCALESIGNATURE, wingdi/PLOCALESIGNATURE'
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
req.typenames: LOCALESIGNATURE, *PLOCALESIGNATURE, *LPLOCALESIGNATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLOCALESIGNATURE
 - wingdi/tagLOCALESIGNATURE
 - PLOCALESIGNATURE
 - wingdi/PLOCALESIGNATURE
 - LOCALESIGNATURE
 - wingdi/LOCALESIGNATURE
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
 - LOCALESIGNATURE
---

# LOCALESIGNATURE structure


## -description

Contains extended font signature information, including two code page bitfields (CPBs) that define the default and supported character sets and code pages. This structure is typically used to represent the relationships between font coverage and locales.

## -struct-fields

### -field lsUsb

A 128-bit Unicode subset bitfield (USB) identifying up to 122 Unicode subranges. Each bit, except the five most significant bits, represents a single subrange. The most significant bit is always 1; the second most significant is reserved and must be 0. Unicode subsets are numbered in accordance with the <a href="/windows/desktop/Intl/opentype-font-format">OpenType font specification</a>. For a list of possible bitfield values, see <a href="/windows/desktop/Intl/unicode-subset-bitfields">Unicode Subset Bitfields</a>.

### -field lsCsbDefault

A code page bitfield that indicates the default OEM and ANSI code pages for a locale. The code pages can be identified by separate bits or a single bit representing a common ANSI and OEM code page. For a list of possible bitfield values, see <a href="/windows/desktop/Intl/code-page-bitfields">Code Page Bitfields</a>.

### -field lsCsbSupported

A code page bitfield that indicates all the code pages in which the locale can be supported. For a list of possible bitfield values, see <a href="/windows/desktop/Intl/code-page-bitfields">Code Page Bitfields</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-fontsignature">FONTSIGNATURE</a>



<a href="/windows/desktop/Intl/unicode-and-character-set-structures">Unicode and Character Set Structures</a>