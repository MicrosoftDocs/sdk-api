---
UID: NF:wingdi.GetKValue
title: GetKValue macro (wingdi.h)
description: The GetKValue macro retrieves the black color value from a CMYK color value.
helpviewer_keywords: ["GetKValue","GetKValue macro [Windows Color System]","_color_GetKValue","wcs.getkvalue","wingdi/GetKValue"]
old-location: wcs\getkvalue.htm
tech.root: WCS
ms.assetid: 8015689c-920c-4896-a34f-cda4f9b187e1
ms.date: 07/01/2025
ms.keywords: GetKValue, GetKValue macro [Windows Color System], _color_GetKValue, wcs.getkvalue, wingdi/GetKValue
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
 - GetKValue
 - wingdi/GetKValue
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
 - GetKValue
---

# GetKValue macro

## -syntax

```cpp
BYTE GetKValue(
     cmyk
);
```

## -returns

Type: **[BYTE](/windows/desktop/winprog/windows-data-types)**

The black color value from a CMYK color value.


## -description

The <b>GetKValue</b> macro retrieves the black color value from a CMYK color value.

## -parameters

### -param cmyk

CMYK color value from which the black color value will be retrieved.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [CMYK](/windows/win32/api/wingdi/nf-wingdi-cmyk)
* [GetCValue](/windows/desktop/api/wingdi/nf-wingdi-getcvalue)
* [GetMValue](/windows/desktop/api/wingdi/nf-wingdi-getmvalue)
* [GetYValue](/windows/desktop/api/wingdi/nf-wingdi-getyvalue)
* [Macros for CMYK values and colors](/windows/win32/wcs/macros-for-cmyk-values-and-colors)
