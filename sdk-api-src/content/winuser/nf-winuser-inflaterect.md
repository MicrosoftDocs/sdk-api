---
UID: NF:winuser.InflateRect
title: InflateRect function (winuser.h)
description: The InflateRect function increases or decreases the width and height of the specified rectangle.
helpviewer_keywords: ["InflateRect","InflateRect function [Windows GDI]","_win32_InflateRect","gdi.inflaterect","winuser/InflateRect"]
old-location: gdi\inflaterect.htm
tech.root: gdi
ms.assetid: 9a52fb7f-cd35-4426-8753-c26cebef30d5
ms.date: 12/05/2018
ms.keywords: InflateRect, InflateRect function [Windows GDI], _win32_InflateRect, gdi.inflaterect, winuser/InflateRect
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
 - InflateRect
 - winuser/InflateRect
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
 - InflateRect
---

# InflateRect function


## -description

The <b>InflateRect</b> function increases or decreases the width and height of the specified rectangle. The <b>InflateRect</b> function adds <i>-dx</i> units to the left end and <i>dx</i> to the right end of the rectangle and <i>-dy</i> units to the top and <i>dy</i> to the bottom. The <i>dx</i> and <i>dy</i> parameters are signed values; positive values increase the width and height, and negative values decrease them.

## -parameters

### -param lprc [in, out]

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that increases or decreases in size.

### -param dx [in]

The amount to increase or decrease the rectangle width. This parameter must be negative to decrease the width.

### -param dy [in]

The amount to increase or decrease the rectangle height. This parameter must be negative to decrease the height.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-intersectrect">IntersectRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-offsetrect">OffsetRect</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/gdi/rectangle-functions">Rectangle Functions</a>



<a href="/windows/desktop/gdi/rectangles">Rectangles Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unionrect">UnionRect</a>