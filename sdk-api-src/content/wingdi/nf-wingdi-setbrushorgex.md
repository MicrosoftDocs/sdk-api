---
UID: NF:wingdi.SetBrushOrgEx
title: SetBrushOrgEx function (wingdi.h)
description: The SetBrushOrgEx function sets the brush origin that GDI assigns to the next brush an application selects into the specified device context.
helpviewer_keywords: ["SetBrushOrgEx","SetBrushOrgEx function [Windows GDI]","_win32_SetBrushOrgEx","gdi.setbrushorgex","wingdi/SetBrushOrgEx"]
old-location: gdi\setbrushorgex.htm
tech.root: gdi
ms.assetid: dcc7575a-49fd-4306-8baa-57e9e0d5ed1f
ms.date: 12/05/2018
ms.keywords: SetBrushOrgEx, SetBrushOrgEx function [Windows GDI], _win32_SetBrushOrgEx, gdi.setbrushorgex, wingdi/SetBrushOrgEx
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
 - SetBrushOrgEx
 - wingdi/SetBrushOrgEx
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
 - SetBrushOrgEx
---

# SetBrushOrgEx function


## -description

The <b>SetBrushOrgEx</b> function sets the brush origin that GDI assigns to the next brush an application selects into the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param x [in]

The x-coordinate, in device units, of the new brush origin. If this value is greater than the brush width, its value is reduced using the modulus operator (<i>nXOrg</i> <b>mod</b> brush width).

### -param y [in]

The y-coordinate, in device units, of the new brush origin. If this value is greater than the brush height, its value is reduced using the modulus operator (<i>nYOrg</i> <b>mod</b> brush height).

### -param lppt [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the previous brush origin.

This parameter can be <b>NULL</b> if the previous brush origin is not required.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

A brush is a bitmap that the system uses to paint the interiors of filled shapes.

The brush origin is a pair of coordinates specifying the location of one pixel in the bitmap. The default brush origin coordinates are (0,0). For horizontal coordinates, the value 0 corresponds to the leftmost column of pixels; the width corresponds to the rightmost column. For vertical coordinates, the value 0 corresponds to the uppermost row of pixels; the height corresponds to the lowermost row.

The system automatically tracks the origin of all window-managed device contexts and adjusts their brushes as necessary to maintain an alignment of patterns on the surface. The brush origin that is set with this call is relative to the upper-left corner of the client area.

An application should call <b>SetBrushOrgEx</b> after setting the bitmap stretching mode to HALFTONE by using <a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a>. This must be done to avoid brush misalignment.

The system automatically tracks the origin of all window-managed device contexts and adjusts their brushes as necessary to maintain an alignment of patterns on the surface.

## -see-also

<a href="/windows/desktop/gdi/brush-functions">Brush Functions</a>



<a href="/windows/desktop/gdi/brushes">Brushes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbrushorgex">GetBrushOrgEx</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-unrealizeobject">UnrealizeObject</a>