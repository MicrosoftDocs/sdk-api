---
UID: NF:wingdi.GetMValue
title: GetMValue macro (wingdi.h)
description: The GetMValue macro retrieves the magenta color value from a CMYK color value.
helpviewer_keywords: ["GetMValue","GetMValue macro [Windows Color System]","_color_GetMValue","wcs.getmvalue","wingdi/GetMValue"]
old-location: wcs\getmvalue.htm
tech.root: WCS
ms.assetid: d24816de-a3c7-4d9f-b6a0-652330cd3ccd
ms.date: 07/01/2025
ms.keywords: GetMValue, GetMValue macro [Windows Color System], _color_GetMValue, wcs.getmvalue, wingdi/GetMValue
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
 - GetMValue
 - wingdi/GetMValue
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
 - GetMValue
---

# GetMValue macro

## -syntax

```cpp
BYTE GetMValue(
     cmyk
);
```

## -returns

Type: **[BYTE](/windows/desktop/winprog/windows-data-types)**

The magenta color value from a CMYK color value.


## -description

The <b>GetMValue</b> macro retrieves the magenta color value from a CMYK color value.

## -parameters

### -param cmyk

CMYK color value from which the magenta color value will be retrieved.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [CMYK](/windows/win32/api/wingdi/nf-wingdi-cmyk)
* [GetCValue](/windows/desktop/api/wingdi/nf-wingdi-getcvalue)
* [GetKValue](/windows/desktop/api/wingdi/nf-wingdi-getkvalue)
* [GetYValue](/windows/desktop/api/wingdi/nf-wingdi-getyvalue)
* [Macros for CMYK values and colors](/windows/win32/wcs/macros-for-cmyk-values-and-colors)
