---
UID: NF:winuser.SetRect
title: SetRect function (winuser.h)
description: The SetRect function sets the coordinates of the specified rectangle. This is equivalent to assigning the left, top, right, and bottom arguments to the appropriate members of the RECT structure.
helpviewer_keywords: ["SetRect","SetRect function [Windows GDI]","_win32_SetRect","gdi.setrect","winuser/SetRect"]
old-location: gdi\setrect.htm
tech.root: gdi
ms.assetid: 346c573b-eaf7-4ca6-bd36-18074f7eccf5
ms.date: 12/05/2018
ms.keywords: SetRect, SetRect function [Windows GDI], _win32_SetRect, gdi.setrect, winuser/SetRect
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
 - SetRect
 - winuser/SetRect
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
 - SetRect
---

# SetRect function


## -description

The <b>SetRect</b> function sets the coordinates of the specified rectangle. This is equivalent to assigning the left, top, right, and bottom arguments to the appropriate members of the <b>RECT</b> structure.

## -parameters

### -param lprc [out]

Pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the rectangle to be set.

### -param xLeft [in]

Specifies the x-coordinate of the rectangle's upper-left corner.

### -param yTop [in]

Specifies the y-coordinate of the rectangle's upper-left corner.

### -param xRight [in]

Specifies the x-coordinate of the rectangle's lower-right corner.

### -param yBottom [in]

Specifies the y-coordinate of the rectangle's lower-right corner.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-rectangles">Using Rectangles</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-copyrect">CopyRect</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/gdi/rectangle-functions">Rectangle Functions</a>



<a href="/windows/desktop/gdi/rectangles">Rectangles Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setrectempty">SetRectEmpty</a>