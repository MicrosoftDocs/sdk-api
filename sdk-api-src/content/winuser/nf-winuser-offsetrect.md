---
UID: NF:winuser.OffsetRect
title: OffsetRect function (winuser.h)
description: The OffsetRect function moves the specified rectangle by the specified offsets.
helpviewer_keywords: ["OffsetRect","OffsetRect function [Windows GDI]","_win32_OffsetRect","gdi.offsetrect","winuser/OffsetRect"]
old-location: gdi\offsetrect.htm
tech.root: gdi
ms.assetid: 14101ad3-8c6e-459a-974a-1a8a4d8d7906
ms.date: 12/05/2018
ms.keywords: OffsetRect, OffsetRect function [Windows GDI], _win32_OffsetRect, gdi.offsetrect, winuser/OffsetRect
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
 - OffsetRect
 - winuser/OffsetRect
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
 - OffsetRect
---

# OffsetRect function


## -description

The <b>OffsetRect</b> function moves the specified rectangle by the specified offsets.

## -parameters

### -param lprc [in, out]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the logical coordinates of the rectangle to be moved.

### -param dx [in]

Specifies the amount to move the rectangle left or right. This parameter must be a negative value to move the rectangle to the left.

### -param dy [in]

Specifies the amount to move the rectangle up or down. This parameter must be a negative value to move the rectangle up.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-rectangles">Using Rectangles</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-inflaterect">InflateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-intersectrect">IntersectRect</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/gdi/rectangle-functions">Rectangle Functions</a>



<a href="/windows/desktop/gdi/rectangles">Rectangles Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unionrect">UnionRect</a>