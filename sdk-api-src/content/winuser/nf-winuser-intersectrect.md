---
UID: NF:winuser.IntersectRect
title: IntersectRect function (winuser.h)
description: The IntersectRect function calculates the intersection of two source rectangles and places the coordinates of the intersection rectangle into the destination rectangle.
helpviewer_keywords: ["IntersectRect","IntersectRect function [Windows GDI]","_win32_IntersectRect","gdi.intersectrect","winuser/IntersectRect"]
old-location: gdi\intersectrect.htm
tech.root: gdi
ms.assetid: da686f78-e557-4ff2-9f24-b229f0c01563
ms.date: 12/05/2018
ms.keywords: IntersectRect, IntersectRect function [Windows GDI], _win32_IntersectRect, gdi.intersectrect, winuser/IntersectRect
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
 - IntersectRect
 - winuser/IntersectRect
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
 - IntersectRect
---

# IntersectRect function


## -description

The <b>IntersectRect</b> function calculates the intersection of two source rectangles and places the coordinates of the intersection rectangle into the destination rectangle. If the source rectangles do not intersect, an empty rectangle (in which all coordinates are set to zero) is placed into the destination rectangle.

## -parameters

### -param lprcDst [out]

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that is to receive the intersection of the rectangles pointed to by the <i>lprcSrc1</i> and <i>lprcSrc2</i> parameters. This parameter cannot be <b>NULL</b>.

### -param lprcSrc1 [in]

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the first source rectangle.

### -param lprcSrc2 [in]

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the second source rectangle.

## -returns

If the rectangles intersect, the return value is nonzero.

If the rectangles do not intersect, the return value is zero.

## -remarks

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-rectangles">Using Rectangles</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-inflaterect">InflateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-offsetrect">OffsetRect</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/gdi/rectangle-functions">Rectangle Functions</a>



<a href="/windows/desktop/gdi/rectangles">Rectangles Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unionrect">UnionRect</a>