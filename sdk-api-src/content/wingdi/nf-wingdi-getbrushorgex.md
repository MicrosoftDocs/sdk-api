---
UID: NF:wingdi.GetBrushOrgEx
title: GetBrushOrgEx function (wingdi.h)
description: The GetBrushOrgEx function retrieves the current brush origin for the specified device context. This function replaces the GetBrushOrg function.
helpviewer_keywords: ["GetBrushOrgEx","GetBrushOrgEx function [Windows GDI]","_win32_GetBrushOrgEx","gdi.getbrushorgex","wingdi/GetBrushOrgEx"]
old-location: gdi\getbrushorgex.htm
tech.root: gdi
ms.assetid: 0b938237-cb06-4776-86f8-14478abcee00
ms.date: 12/05/2018
ms.keywords: GetBrushOrgEx, GetBrushOrgEx function [Windows GDI], _win32_GetBrushOrgEx, gdi.getbrushorgex, wingdi/GetBrushOrgEx
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
 - GetBrushOrgEx
 - wingdi/GetBrushOrgEx
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
 - GetBrushOrgEx
---

# GetBrushOrgEx function


## -description

The <b>GetBrushOrgEx</b> function retrieves the current brush origin for the specified device context. This function replaces the <b>GetBrushOrg</b> function.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lppt [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the brush origin, in device coordinates.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

A brush is a bitmap that the system uses to paint the interiors of filled shapes.

The brush origin is a set of coordinates with values between 0 and 7, specifying the location of one pixel in the bitmap. The default brush origin coordinates are (0,0). For horizontal coordinates, the value 0 corresponds to the leftmost column of pixels; the value 7 corresponds to the rightmost column. For vertical coordinates, the value 0 corresponds to the uppermost row of pixels; the value 7 corresponds to the lowermost row. When the system positions the brush at the start of any painting operation, it maps the origin of the brush to the location in the window's client area specified by the brush origin. For example, if the origin is set to (2,3), the system maps the origin of the brush (0,0) to the location (2,3) on the window's client area.

If an application uses a brush to fill the backgrounds of both a parent and a child window with matching colors, it may be necessary to set the brush origin after painting the parent window but before painting the child window.

The system automatically tracks the origin of all window-managed device contexts and adjusts their brushes as necessary to maintain an alignment of patterns on the surface.

## -see-also

<a href="/windows/desktop/gdi/brush-functions">Brush Functions</a>



<a href="/windows/desktop/gdi/brushes">Brushes Overview</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbrushorgex">SetBrushOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-unrealizeobject">UnrealizeObject</a>