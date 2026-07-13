---
UID: NF:winuser.DrawFocusRect
title: DrawFocusRect function (winuser.h)
description: The DrawFocusRect function draws a rectangle in the style used to indicate that the rectangle has the focus.
helpviewer_keywords: ["DrawFocusRect","DrawFocusRect function [Windows GDI]","_win32_DrawFocusRect","gdi.drawfocusrect","winuser/DrawFocusRect"]
old-location: gdi\drawfocusrect.htm
tech.root: gdi
ms.assetid: a910d04f-fe4d-4fc9-a518-abac864da6f3
ms.date: 12/05/2018
ms.keywords: DrawFocusRect, DrawFocusRect function [Windows GDI], _win32_DrawFocusRect, gdi.drawfocusrect, winuser/DrawFocusRect
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
 - DrawFocusRect
 - winuser/DrawFocusRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-draw-l1-1-0.dll
 - user32.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-0.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - DrawFocusRect
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# DrawFocusRect function


## -description

The <b>DrawFocusRect</b> function draws a rectangle in the style used to indicate that the rectangle has the focus.

## -parameters

### -param hDC [in]

A handle to the device context.

### -param lprc [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the logical coordinates of the rectangle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

<b>DrawFocusRect</b> works only in MM_TEXT mode.

Because <b>DrawFocusRect</b> is an XOR function, calling it a second time with the same rectangle removes the rectangle from the screen.

This function draws a rectangle that cannot be scrolled. To scroll an area containing a rectangle drawn by this function, call <b>DrawFocusRect</b> to remove the rectangle from the screen, scroll the area, and then call <b>DrawFocusRect</b> again to draw the rectangle in the new position.

<b>Windows XP:</b> The focus rectangle can now be thicker than 1 pixel, so it is more visible for high-resolution, high-density displays and accessibility needs. This is handled by the SPI_SETFOCUSBORDERWIDTH and SPI_SETFOCUSBORDERHEIGHT in <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>.


#### Examples

For an example, see "Creating an Owner-Drawn List Box" in <a href="/windows/desktop/Controls/using-list-boxes">Using List Boxes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-framerect">FrameRect</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>
