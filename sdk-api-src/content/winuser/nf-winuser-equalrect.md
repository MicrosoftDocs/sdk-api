---
UID: NF:winuser.EqualRect
title: EqualRect function (winuser.h)
description: The EqualRect function determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.
helpviewer_keywords: ["EqualRect","EqualRect function [Windows GDI]","_win32_EqualRect","gdi.equalrect","winuser/EqualRect"]
old-location: gdi\equalrect.htm
tech.root: gdi
ms.assetid: 00763184-6b60-4095-b71e-5a851c2643aa
ms.date: 12/05/2018
ms.keywords: EqualRect, EqualRect function [Windows GDI], _win32_EqualRect, gdi.equalrect, winuser/EqualRect
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
 - EqualRect
 - winuser/EqualRect
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
 - EqualRect
---

# EqualRect function


## -description

The <b>EqualRect</b> function determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.

## -parameters

### -param lprc1 [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the logical coordinates of the first rectangle.

### -param lprc2 [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the logical coordinates of the second rectangle.

## -returns

If the two rectangles are identical, the return value is nonzero.

If the two rectangles are not identical, the return value is zero.

## -remarks

The <b>EqualRect</b> function does not treat empty rectangles as equal if their coordinates are different.

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-isrectempty">IsRectEmpty</a>



<a href="/windows/desktop/api/winuser/nf-winuser-ptinrect">PtInRect</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/gdi/rectangle-functions">Rectangle Functions</a>



<a href="/windows/desktop/gdi/rectangles">Rectangles Overview</a>