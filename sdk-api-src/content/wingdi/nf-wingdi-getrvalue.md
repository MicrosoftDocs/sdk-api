---
UID: NF:wingdi.GetRValue
title: GetRValue macro (wingdi.h)
description: The GetRValue macro retrieves an intensity value for the red component of a red, green, blue (RGB) value.
helpviewer_keywords: ["GetRValue","GetRValue macro [Windows GDI]","_win32_GetRValue","gdi.getrvalue","wingdi/GetRValue"]
old-location: gdi\getrvalue.htm
tech.root: gdi
ms.assetid: c183b671-20f8-468c-af0d-9f03cbc4b170
ms.date: 07/01/2025
ms.keywords: GetRValue, GetRValue macro [Windows GDI], _win32_GetRValue, gdi.getrvalue, wingdi/GetRValue
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
 - GetRValue
 - wingdi/GetRValue
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
 - GetRValue
---

# GetRValue macro

## -syntax

```cpp
BYTE GetRValue(
    DWORD rgb
);
```

## -returns

Type: **[BYTE](/windows/desktop/winprog/windows-data-types)**

The return value is the intensity of the red component of the specified RGB color.


## -description

The <b>GetRValue</b> macro retrieves an intensity value for the red component of a red, green, blue (RGB) value.

## -parameters

### -param rgb

Specifies an RGB color value.

## -remarks

The intensity value is in the range 0 through 255.

## -see-also

<a href="/windows/desktop/gdi/color-macros">Color Macros</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbvalue">GetBValue</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getgvalue">GetGValue</a>



<a href="/previous-versions/dd162770(v=vs.85)">PALETTEINDEX</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-palettergb">PALETTERGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
