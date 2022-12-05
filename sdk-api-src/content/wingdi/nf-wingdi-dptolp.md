---
UID: NF:wingdi.DPtoLP
title: DPtoLP function (wingdi.h)
description: The DPtoLP function converts device coordinates into logical coordinates. The conversion depends on the mapping mode of the device context, the settings of the origins and extents for the window and viewport, and the world transformation.
helpviewer_keywords: ["DPtoLP","DPtoLP function [Windows GDI]","_win32_DPtoLP","gdi.dptolp","wingdi/DPtoLP"]
old-location: gdi\dptolp.htm
tech.root: gdi
ms.assetid: 0106867c-e8c5-4826-8cba-60c29e1d021a
ms.date: 12/05/2018
ms.keywords: DPtoLP, DPtoLP function [Windows GDI], _win32_DPtoLP, gdi.dptolp, wingdi/DPtoLP
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
 - DPtoLP
 - wingdi/DPtoLP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - DPtoLP
---

# DPtoLP function


## -description

The <b>DPtoLP</b> function converts device coordinates into logical coordinates. The conversion depends on the mapping mode of the device context, the settings of the origins and extents for the window and viewport, and the world transformation.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lppt [in, out]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures. The x- and y-coordinates contained in each <b>POINT</b> structure will be transformed.

### -param c [in]

The number of points in the array.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>DPtoLP</b> function fails if the device coordinates exceed 27 bits, or if the converted logical coordinates exceed 32 bits. In the case of such an overflow, the results for all the points are undefined.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-coordinate-spaces-and-transformations">Using Coordinate Spaces and Transformations</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-lptodp">LPtoDP</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>