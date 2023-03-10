---
UID: NF:wingdi.ScaleViewportExtEx
title: ScaleViewportExtEx function (wingdi.h)
description: The ScaleViewportExtEx function modifies the viewport for a device context using the ratios formed by the specified multiplicands and divisors.
helpviewer_keywords: ["ScaleViewportExtEx","ScaleViewportExtEx function [Windows GDI]","_win32_ScaleViewportExtEx","gdi.scaleviewportextex","wingdi/ScaleViewportExtEx"]
old-location: gdi\scaleviewportextex.htm
tech.root: gdi
ms.assetid: 8dde1322-82d7-4069-9655-a7bd3a324cb0
ms.date: 12/05/2018
ms.keywords: ScaleViewportExtEx, ScaleViewportExtEx function [Windows GDI], _win32_ScaleViewportExtEx, gdi.scaleviewportextex, wingdi/ScaleViewportExtEx
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
 - ScaleViewportExtEx
 - wingdi/ScaleViewportExtEx
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
 - ScaleViewportExtEx
---

# ScaleViewportExtEx function


## -description

The <b>ScaleViewportExtEx</b> function modifies the viewport for a device context using the ratios formed by the specified multiplicands and divisors.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param xn [in]

The amount by which to multiply the current horizontal extent.

### -param dx [in]

The amount by which to divide the current horizontal extent.

### -param yn [in]

The amount by which to multiply the current vertical extent.

### -param yd [in]

The amount by which to divide the current vertical extent.

### -param lpsz [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that receives the previous viewport extents, in device units. If <i>lpSize</i> is <b>NULL</b>, this parameter is not used.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The viewport extents are modified as follows:


```cpp

    xNewVE = (xOldVE * Xnum) / Xdenom 
    yNewVE = (yOldVE * Ynum) / Ydenom 

```

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getviewportextex">GetViewportExtEx</a>



<a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>