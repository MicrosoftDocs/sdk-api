---
UID: NS:wingdi.tagWCRANGE
title: WCRANGE (wingdi.h)
description: The WCRANGE structure specifies a range of Unicode characters.
helpviewer_keywords: ["*LPWCRANGE","*PWCRANGE","PWCRANGE","PWCRANGE structure pointer [Windows GDI]","WCRANGE","WCRANGE structure [Windows GDI]","_win32_WCRANGE_str","gdi.wcrange","wingdi/PWCRANGE","wingdi/WCRANGE"]
old-location: gdi\wcrange.htm
tech.root: gdi
ms.assetid: 20959057-6062-4c1e-a23d-535584ba6ea3
ms.date: 12/05/2018
ms.keywords: '*LPWCRANGE, *PWCRANGE, PWCRANGE, PWCRANGE structure pointer [Windows GDI], WCRANGE, WCRANGE structure [Windows GDI], _win32_WCRANGE_str, gdi.wcrange, wingdi/PWCRANGE, wingdi/WCRANGE'
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
req.typenames: WCRANGE, *PWCRANGE, *LPWCRANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWCRANGE
 - wingdi/tagWCRANGE
 - PWCRANGE
 - wingdi/PWCRANGE
 - WCRANGE
 - wingdi/WCRANGE
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
 - WCRANGE
---

# WCRANGE structure


## -description

The <b>WCRANGE</b> structure specifies a range of Unicode characters.

## -struct-fields

### -field wcLow

Low Unicode code point in the range of supported Unicode code points.

### -field cGlyphs

Number of supported Unicode code points in this range.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-glyphset">GLYPHSET</a>