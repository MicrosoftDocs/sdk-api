---
UID: NF:wingdi.PALETTEINDEX
title: PALETTEINDEX macro (wingdi.h)
description: The PALETTEINDEX macro accepts an index to a logical-color palette entry and returns a palette-entry specifier consisting of a COLORREF value that specifies the color associated with the given index.
helpviewer_keywords: ["PALETTEINDEX","PALETTEINDEX macro [Windows GDI]","_win32_PALETTEINDEX","gdi.paletteindex","wingdi/PALETTEINDEX"]
old-location: gdi\paletteindex.htm
tech.root: gdi
ms.assetid: 76d859fa-11a5-451f-9d7a-9cf0740eca36
ms.date: 07/01/2025
ms.keywords: PALETTEINDEX, PALETTEINDEX macro [Windows GDI], _win32_PALETTEINDEX, gdi.paletteindex, wingdi/PALETTEINDEX
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PALETTEINDEX
 - wingdi/PALETTEINDEX
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
 - PALETTEINDEX
---

# PALETTEINDEX macro

## -syntax

```cpp
COLORREF PALETTEINDEX(
    WORD i
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

The return value is a logical-palette index specifier.


## -description

The <b>PALETTEINDEX</b> macro accepts an index to a logical-color palette entry and returns a palette-entry specifier consisting of a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value that specifies the color associated with the given index. An application using a logical palette can pass this specifier, instead of an explicit red, green, blue (RGB) value, to GDI functions that expect a color. This allows the function to use the color in the specified palette entry.

## -parameters

### -param i

An index to the palette entry containing the color to be used for a graphics operation.

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/gdi/color-macros">Color Macros</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-palettergb">PALETTERGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
