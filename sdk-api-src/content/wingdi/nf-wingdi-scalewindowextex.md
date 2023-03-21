---
UID: NF:wingdi.ScaleWindowExtEx
title: ScaleWindowExtEx function (wingdi.h)
description: The ScaleWindowExtEx function modifies the window for a device context using the ratios formed by the specified multiplicands and divisors.
helpviewer_keywords: ["ScaleWindowExtEx","ScaleWindowExtEx function [Windows GDI]","_win32_ScaleWindowExtEx","gdi.scalewindowextex","wingdi/ScaleWindowExtEx"]
old-location: gdi\scalewindowextex.htm
tech.root: gdi
ms.assetid: c34f0978-74dd-4839-99f2-a106f3d2c0f9
ms.date: 12/05/2018
ms.keywords: ScaleWindowExtEx, ScaleWindowExtEx function [Windows GDI], _win32_ScaleWindowExtEx, gdi.scalewindowextex, wingdi/ScaleWindowExtEx
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ScaleWindowExtEx
 - wingdi/ScaleWindowExtEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - ScaleWindowExtEx
---

# ScaleWindowExtEx function


## -description

The <b>ScaleWindowExtEx</b> function modifies the window for a device context using the ratios formed by the specified multiplicands and divisors.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param xn [in]

The amount by which to multiply the current horizontal extent.

### -param xd [in]

The amount by which to divide the current horizontal extent.

### -param yn [in]

The amount by which to multiply the current vertical extent.

### -param yd [in]

The amount by which to divide the current vertical extent.

### -param lpsz [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that receives the previous window extents, in logical units. If <i>lpSize</i> is <b>NULL</b>, this parameter is not used.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The window extents are modified as follows:


```cpp

    xNewWE = (xOldWE * Xnum) / Xdenom 
    yNewWE = (yOldWE * Ynum) / Ydenom 

```

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getwindowextex">GetWindowExtEx</a>



<a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>