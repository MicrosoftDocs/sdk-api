---
UID: NF:wingdi.GetCValue
title: GetCValue macro (wingdi.h)
description: The GetCValue macro retrieves the cyan color value from a CMYK color value.
helpviewer_keywords: ["GetCValue","GetCValue macro [Windows Color System]","_color_GetCValue","wcs.getcvalue","wingdi/GetCValue"]
old-location: wcs\getcvalue.htm
tech.root: WCS
ms.assetid: 0b1b1eca-61b2-4011-85ea-6311ac78cab6
ms.date: 07/01/2025
ms.keywords: GetCValue, GetCValue macro [Windows Color System], _color_GetCValue, wcs.getcvalue, wingdi/GetCValue
req.header: wingdi.h
req.include-header: 
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
 - GetCValue
 - wingdi/GetCValue
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
 - GetCValue
---

# GetCValue macro

## -syntax

```cpp
BYTE GetCValue(
     cmyk
);
```

## -returns

Type: **[BYTE](/windows/desktop/winprog/windows-data-types)**

The cyan color value from a CMYK color value.


## -description

The <b>GetCValue</b> macro retrieves the cyan color value from a CMYK color value.

## -parameters

### -param cmyk

CMYK color value from which the cyan color value will be retrieved.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [CMYK](/windows/win32/api/wingdi/nf-wingdi-cmyk)
* [GetKValue](/windows/desktop/api/wingdi/nf-wingdi-getkvalue)
* [GetMValue](/windows/desktop/api/wingdi/nf-wingdi-getmvalue)
* [GetYValue](/windows/desktop/api/wingdi/nf-wingdi-getyvalue)
* [Macros for CMYK values and colors](/windows/win32/wcs/macros-for-cmyk-values-and-colors)
