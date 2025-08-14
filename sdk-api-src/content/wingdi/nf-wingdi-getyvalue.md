---
UID: NF:wingdi.GetYValue
title: GetYValue macro (wingdi.h)
description: The GetYValue macro retrieves the yellow color value from a CMYK color value.
helpviewer_keywords: ["GetYValue","GetYValue macro [Windows Color System]","_color_GetYValue","wcs.getyvalue","wingdi/GetYValue"]
old-location: wcs\getyvalue.htm
tech.root: WCS
ms.assetid: 5948db59-649f-4940-afb6-5bdb84544915
ms.date: 07/01/2025
ms.keywords: GetYValue, GetYValue macro [Windows Color System], _color_GetYValue, wcs.getyvalue, wingdi/GetYValue
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
 - GetYValue
 - wingdi/GetYValue
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
 - GetYValue
---

# GetYValue macro

## -syntax

```cpp
BYTE GetYValue(
     cmyk
);
```

## -returns

Type: **[BYTE](/windows/desktop/winprog/windows-data-types)**

The yellow color value from a CMYK color value.


## -description

The <b>GetYValue</b> macro retrieves the yellow color value from a CMYK color value.

## -parameters

### -param cmyk

CMYK color value from which the yellow color value will be retrieved.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [CMYK](/windows/win32/api/wingdi/nf-wingdi-cmyk)
* [GetCValue](/windows/desktop/api/wingdi/nf-wingdi-getcvalue)
* [GetKValue](/windows/desktop/api/wingdi/nf-wingdi-getkvalue)
* [Macros for CMYK values and colors](/windows/win32/wcs/macros-for-cmyk-values-and-colors)
