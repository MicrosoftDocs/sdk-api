---
UID: NF:mmsystem.DIBINDEX
title: DIBINDEX macro (mmsystem.h)
description: The DIBINDEX macro takes an index to an entry in a DIB color table and returns a COLORREF value that specifies the color associated with the given index.
helpviewer_keywords: ["DIBINDEX","DIBINDEX macro [Windows GDI]","_win32_DIBINDEX","gdi.dibindex","mmsystem/DIBINDEX"]
old-location: gdi\dibindex.htm
tech.root: gdi
ms.assetid: a1c2274e-ddcb-4e11-af70-9f79210d2d5f
ms.date: 07/01/2025
ms.keywords: DIBINDEX, DIBINDEX macro [Windows GDI], _win32_DIBINDEX, gdi.dibindex, mmsystem/DIBINDEX
req.header: mmsystem.h
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
 - DIBINDEX
 - mmsystem/DIBINDEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmsystem.h
api_name:
 - DIBINDEX
---

# DIBINDEX macro

## -syntax

```cpp
LONG DIBINDEX(
    WORD n
);
```

## -returns

Type: **LONG**

The return value is a color table index specifier in the form of a 32-bit <a href="/windows/desktop/gdi/colorref">COLORREF</a> value.


## -description

The <b>DIBINDEX</b> macro takes an index to an entry in a DIB color table and returns a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value that specifies the color associated with the given index. An application using a device context with a DIB section selected into it can pass this specifier, instead of an explicit red, green, blue (RGB) value, to GDI functions that expect a color. This allows the function to use the color at the specified color table index.

## -parameters

### -param n

Specifies an index to the color table entry containing the color to be used for a graphics operation.

## -remarks

<b>DIBINDEX</b> indexes colors in a DIB color table in a manner similar to the way <a href="/previous-versions/dd162770(v=vs.85)">PALETTEINDEX</a> indexes colors in a logical palette.

<b>DIBINDEX</b> also works with 16-bit bitmaps and device contexts (DCs).

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/gdi/color-macros">Color Macros</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/previous-versions/dd162770(v=vs.85)">PALETTEINDEX</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
