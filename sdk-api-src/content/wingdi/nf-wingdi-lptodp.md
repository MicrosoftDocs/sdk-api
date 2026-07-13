---
UID: NF:wingdi.LPtoDP
title: LPtoDP function (wingdi.h)
description: The LPtoDP function converts logical coordinates into device coordinates. The conversion depends on the mapping mode of the device context, the settings of the origins and extents for the window and viewport, and the world transformation.
helpviewer_keywords: ["LPtoDP","LPtoDP function [Windows GDI]","_win32_LPtoDP","gdi.lptodp","wingdi/LPtoDP"]
old-location: gdi\lptodp.htm
tech.root: gdi
ms.assetid: 670a16fb-842e-4250-9ad7-dc08e849c2ba
ms.date: 12/05/2018
ms.keywords: LPtoDP, LPtoDP function [Windows GDI], _win32_LPtoDP, gdi.lptodp, wingdi/LPtoDP
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
 - LPtoDP
 - wingdi/LPtoDP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - LPtoDP
---

# LPtoDP function


## -description

The <b>LPtoDP</b> function converts logical coordinates into device coordinates. The conversion depends on the mapping mode of the device context, the settings of the origins and extents for the window and viewport, and the world transformation.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lppt [in, out]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures. The x-coordinates and y-coordinates contained in each of the <b>POINT</b> structures will be transformed.

### -param c [in]

The number of points in the array.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>LPtoDP</b> function fails if the logical coordinates exceed 32 bits, or if the converted device coordinates exceed 27 bits. In the case of such an overflow, the results for all the points are undefined.

<b>LPtoDP</b> calculates complex floating-point arithmetic, and it has a caching system for efficiency. Therefore, the conversion result of an initial call to <b>LPtoDP</b> might not exactly match the conversion result of a later call to <b>LPtoDP</b>. We recommend not to write code that relies on the exact match of the conversion results from multiple calls to <b>LPtoDP</b> even if the parameters that are passed to each call are identical.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-dptolp">DPtoLP</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>