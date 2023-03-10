---
UID: NF:wingdi.GetBitmapDimensionEx
title: GetBitmapDimensionEx function (wingdi.h)
description: The GetBitmapDimensionEx function retrieves the dimensions of a compatible bitmap. The retrieved dimensions must have been set by the SetBitmapDimensionEx function.
helpviewer_keywords: ["GetBitmapDimensionEx","GetBitmapDimensionEx function [Windows GDI]","_win32_GetBitmapDimensionEx","gdi.getbitmapdimensionex","wingdi/GetBitmapDimensionEx"]
old-location: gdi\getbitmapdimensionex.htm
tech.root: gdi
ms.assetid: 3e4f5afc-26d3-4fb2-8d00-183165fdf471
ms.date: 12/05/2018
ms.keywords: GetBitmapDimensionEx, GetBitmapDimensionEx function [Windows GDI], _win32_GetBitmapDimensionEx, gdi.getbitmapdimensionex, wingdi/GetBitmapDimensionEx
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
 - GetBitmapDimensionEx
 - wingdi/GetBitmapDimensionEx
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
 - GetBitmapDimensionEx
---

# GetBitmapDimensionEx function


## -description

The <b>GetBitmapDimensionEx</b> function retrieves the dimensions of a compatible bitmap. The retrieved dimensions must have been set by the <a href="/windows/desktop/api/wingdi/nf-wingdi-setbitmapdimensionex">SetBitmapDimensionEx</a> function.

## -parameters

### -param hbit [in]

A handle to a compatible bitmap (DDB).

### -param lpsize [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure to receive the bitmap dimensions. For more information, see Remarks.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The function returns a data structure that contains fields for the height and width of the bitmap, in .01-mm units. If those dimensions have not yet been set, the structure that is returned will have zeros in those fields.

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbitmapdimensionex">SetBitmapDimensionEx</a>