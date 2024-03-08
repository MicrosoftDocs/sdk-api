---
UID: NF:winuser.PtInRect
title: PtInRect function (winuser.h)
description: The PtInRect function determines whether the specified point lies within the specified rectangle.
helpviewer_keywords: ["PtInRect","PtInRect function [Windows GDI]","_win32_PtInRect","gdi.ptinrect","winuser/PtInRect"]
old-location: gdi\ptinrect.htm
tech.root: gdi
ms.assetid: 8a47a238-082c-44b8-a270-5ebb4d3d9fc8
ms.date: 12/05/2018
ms.keywords: PtInRect, PtInRect function [Windows GDI], _win32_PtInRect, gdi.ptinrect, winuser/PtInRect
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PtInRect
 - winuser/PtInRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - API-MS-Win-NTUser-Rectangle-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Rectangle-Ext-l1-1-0.dll
api_name:
 - PtInRect
---

# PtInRect function


## -description

The <b>PtInRect</b> function determines whether the specified point lies within the specified rectangle. A point is within a rectangle if it lies on the left or top side or is within all four sides. A point on the right or bottom side is considered outside the rectangle.

## -parameters

### -param lprc [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the specified rectangle.

### -param pt [in]

A <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that contains the specified point.

## -returns

If the specified point lies within the rectangle, the return value is nonzero.

If the specified point does not lie within the rectangle, the return value is zero.

## -remarks

The rectangle must be normalized before <b>PtInRect</b> is called. That is, lprc.right must be greater than lprc.left and lprc.bottom must be greater than lprc.top. If the rectangle is not normalized, a point is never considered inside of the rectangle.

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-rectangles">Using Rectangles</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-equalrect">EqualRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-isrectempty">IsRectEmpty</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/gdi/rectangle-functions">Rectangle Functions</a>



<a href="/windows/desktop/gdi/rectangles">Rectangles Overview</a>