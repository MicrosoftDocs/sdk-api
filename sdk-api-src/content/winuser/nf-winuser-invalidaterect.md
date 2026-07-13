---
UID: NF:winuser.InvalidateRect
title: InvalidateRect function (winuser.h)
description: The InvalidateRect function adds a rectangle to the specified window's update region. The update region represents the portion of the window's client area that must be redrawn.
helpviewer_keywords: ["InvalidateRect","InvalidateRect function [Windows GDI]","_win32_InvalidateRect","gdi.invalidaterect","winuser/InvalidateRect"]
old-location: gdi\invalidaterect.htm
tech.root: gdi
ms.assetid: 5a823d36-d08b-41c9-8857-540576f54b55
ms.date: 12/05/2018
ms.keywords: InvalidateRect, InvalidateRect function [Windows GDI], _win32_InvalidateRect, gdi.invalidaterect, winuser/InvalidateRect
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
 - InvalidateRect
 - winuser/InvalidateRect
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
 - InvalidateRect
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# InvalidateRect function


## -description

The <b>InvalidateRect</b> function adds a rectangle to the specified window's update region. The update region represents the portion of the window's client area that must be redrawn.

## -parameters

### -param hWnd [in]

A handle to the window whose update region has changed. If this parameter is <b>NULL</b>, the system invalidates and redraws all windows, not just the windows for this application, and sends the <a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a> and <a href="/windows/desktop/gdi/wm-ncpaint">WM_NCPAINT</a> messages before the function returns. Setting this parameter to <b>NULL</b> is not recommended.

### -param lpRect [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the client coordinates of the rectangle to be added to the update region. If this parameter is <b>NULL</b>, the entire client area is added to the update region.

### -param bErase [in]

Specifies whether the background within the update region is to be erased when the update region is processed. If this parameter is <b>TRUE</b>, the background is erased when the <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> function is called. If this parameter is <b>FALSE</b>, the background remains unchanged.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The invalidated areas accumulate in the update region until the region is processed when the next <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message occurs or until the region is validated by using the <a href="/windows/desktop/api/winuser/nf-winuser-validaterect">ValidateRect</a> or <a href="/windows/desktop/api/winuser/nf-winuser-validatergn">ValidateRgn</a> function.

The system sends a <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message to a window whenever its update region is not empty and there are no other messages in the application queue for that window.

If the <i>bErase</i> parameter is <b>TRUE</b> for any part of the update region, the background is erased in the entire region, not just in the specified part.


#### Examples

For an example, see <a href="/windows/desktop/gdi/invalidating-the-client-area">Invalidating the Client Area</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidatergn">InvalidateRgn</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/winuser/nf-winuser-validaterect">ValidateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-validatergn">ValidateRgn</a>



<a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a>



<a href="/windows/desktop/gdi/wm-ncpaint">WM_NCPAINT</a>



<a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a>
