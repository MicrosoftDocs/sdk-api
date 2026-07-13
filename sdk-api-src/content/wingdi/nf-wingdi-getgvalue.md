---
UID: NF:wingdi.GetGValue
title: GetGValue macro (wingdi.h)
description: The GetGValue macro retrieves an intensity value for the green component of a red, green, blue (RGB) value.
helpviewer_keywords: ["GetGValue","GetGValue macro [Windows GDI]","_win32_GetGValue","gdi.getgvalue","wingdi/GetGValue"]
old-location: gdi\getgvalue.htm
tech.root: gdi
ms.assetid: be989b36-8acb-435b-8d71-1c388c7884f0
ms.date: 07/01/2025
ms.keywords: GetGValue, GetGValue macro [Windows GDI], _win32_GetGValue, gdi.getgvalue, wingdi/GetGValue
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
 - GetGValue
 - wingdi/GetGValue
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
 - GetGValue
---

# GetGValue macro

## -syntax

```cpp
BYTE GetGValue(
    DWORD rgb
);
```

## -returns

Type: **[BYTE](/windows/desktop/winprog/windows-data-types)**

The return value is the intensity of the green component of the specified RGB color.


## -description

The <b>GetGValue</b> macro retrieves an intensity value for the green component of a red, green, blue (RGB) value.

## -parameters

### -param rgb

Specifies an RGB color value.

## -remarks

The intensity value is in the range 0 through 255.

## -see-also

<a href="/windows/desktop/gdi/color-macros">Color Macros</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbvalue">GetBValue</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getrvalue">GetRValue</a>



<a href="/previous-versions/dd162770(v=vs.85)">PALETTEINDEX</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-palettergb">PALETTERGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
