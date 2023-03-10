---
UID: NF:winuser.IsRectEmpty
title: IsRectEmpty function (winuser.h)
description: The IsRectEmpty function determines whether the specified rectangle is empty.
helpviewer_keywords: ["IsRectEmpty","IsRectEmpty function [Windows GDI]","_win32_IsRectEmpty","gdi.isrectempty","winuser/IsRectEmpty"]
old-location: gdi\isrectempty.htm
tech.root: gdi
ms.assetid: 9deeed4f-304e-47a3-8259-ed7bc3815fd7
ms.date: 12/05/2018
ms.keywords: IsRectEmpty, IsRectEmpty function [Windows GDI], _win32_IsRectEmpty, gdi.isrectempty, winuser/IsRectEmpty
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
 - IsRectEmpty
 - winuser/IsRectEmpty
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
 - IsRectEmpty
---

# IsRectEmpty function


## -description

The <b>IsRectEmpty</b> function determines whether the specified rectangle is empty. An empty rectangle is one that has no area; that is, the coordinate of the right side is less than or equal to the coordinate of the left side, or the coordinate of the bottom side is less than or equal to the coordinate of the top side.

## -parameters

### -param lprc [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the logical coordinates of the rectangle.

## -returns

If the rectangle is empty, the return value is nonzero.

If the rectangle is not empty, the return value is zero.

## -remarks

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-rectangles">Using Rectangles</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-equalrect">EqualRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-ptinrect">PtInRect</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/gdi/rectangle-functions">Rectangle Functions</a>



<a href="/windows/desktop/gdi/rectangles">Rectangles Overview</a>