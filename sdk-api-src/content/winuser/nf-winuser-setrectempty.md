---
UID: NF:winuser.SetRectEmpty
title: SetRectEmpty function (winuser.h)
description: The SetRectEmpty function creates an empty rectangle in which all coordinates are set to zero.
helpviewer_keywords: ["SetRectEmpty","SetRectEmpty function [Windows GDI]","_win32_SetRectEmpty","gdi.setrectempty","winuser/SetRectEmpty"]
old-location: gdi\setrectempty.htm
tech.root: gdi
ms.assetid: d3c677ae-e45c-4d54-8521-75954a466a68
ms.date: 12/05/2018
ms.keywords: SetRectEmpty, SetRectEmpty function [Windows GDI], _win32_SetRectEmpty, gdi.setrectempty, winuser/SetRectEmpty
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
 - SetRectEmpty
 - winuser/SetRectEmpty
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
 - SetRectEmpty
---

# SetRectEmpty function


## -description

The <b>SetRectEmpty</b> function creates an empty rectangle in which all coordinates are set to zero.

## -parameters

### -param lprc [out]

Pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the coordinates of the rectangle.

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



<a href="/windows/desktop/api/winuser/nf-winuser-setrect">SetRect</a>