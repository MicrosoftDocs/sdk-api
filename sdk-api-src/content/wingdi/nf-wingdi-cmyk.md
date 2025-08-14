---
UID: NF:wingdi.CMYK
title: CMYK macro (wingdi.h)
description: The CMYK macro creates a CMYK color value by combining the specified cyan, magenta, yellow, and black values.
helpviewer_keywords: ["CMYK","CMYK macro [Windows Color System]","_color_CMYK","wcs.cmyk","wingdi/CMYK"]
old-location: wcs\cmyk.htm
tech.root: WCS
ms.assetid: ee28d4e3-314f-429d-841b-da432ff6dc78
ms.date: 07/01/2025
ms.keywords: CMYK, CMYK macro [Windows Color System], _color_CMYK, wcs.cmyk, wingdi/CMYK
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
 - CMYK
 - wingdi/CMYK
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
 - CMYK
---

# CMYK macro

## -syntax

```cpp
COLORREF CMYK(
     c,
     m,
     y,
     k
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

A CMYK color value.


## -description

The <b>CMYK</b> macro creates a CMYK color value by combining the specified cyan, magenta, yellow, and black values.

## -parameters

### -param c

The cyan value for the color to be created.

### -param m

The magenta value for the color to be created.

### -param y

The yellow value for the color to be created.

### -param k

The black value for the color to be created.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [GetCValue](/windows/desktop/api/wingdi/nf-wingdi-getcvalue)
* [GetKValue](/windows/desktop/api/wingdi/nf-wingdi-getkvalue)
* [GetMValue](/windows/desktop/api/wingdi/nf-wingdi-getmvalue)
* [GetYValue](/windows/desktop/api/wingdi/nf-wingdi-getyvalue)
* [Macros for CMYK values and colors](/windows/win32/wcs/macros-for-cmyk-values-and-colors)
