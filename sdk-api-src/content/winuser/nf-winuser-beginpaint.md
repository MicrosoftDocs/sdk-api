---
UID: NF:winuser.BeginPaint
title: BeginPaint function (winuser.h)
description: The BeginPaint function prepares the specified window for painting and fills a PAINTSTRUCT structure with information about the painting.
helpviewer_keywords: ["BeginPaint","BeginPaint function [Windows GDI]","_win32_BeginPaint","gdi.beginpaint","winuser/BeginPaint"]
old-location: gdi\beginpaint.htm
tech.root: gdi
ms.assetid: 513341d7-bed8-469c-a067-ee71dc8860f9
ms.date: 12/05/2018
ms.keywords: BeginPaint, BeginPaint function [Windows GDI], _win32_BeginPaint, gdi.beginpaint, winuser/BeginPaint
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
 - BeginPaint
 - winuser/BeginPaint
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
 - BeginPaint
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# BeginPaint function


## -description

The <b>BeginPaint</b> function prepares the specified window for painting and fills a <a href="/windows/desktop/api/winuser/ns-winuser-paintstruct">PAINTSTRUCT</a> structure with information about the painting.

## -parameters

### -param hWnd [in]

Handle to the window to be repainted.

### -param lpPaint [out]

Pointer to the <a href="/windows/desktop/api/winuser/ns-winuser-paintstruct">PAINTSTRUCT</a> structure that will receive painting information.

## -returns

If the function succeeds, the return value is the handle to a display device context for the specified window.

If the function fails, the return value is <b>NULL</b>, indicating that no display device context is available.

## -remarks

The <b>BeginPaint</b> function automatically sets the clipping region of the device context to exclude any area outside the update region. The update region is set by the <a href="/windows/desktop/api/winuser/nf-winuser-invalidaterect">InvalidateRect</a> or <a href="/windows/desktop/api/winuser/nf-winuser-invalidatergn">InvalidateRgn</a> function and by the system after sizing, moving, creating, scrolling, or any other operation that affects the client area. If the update region is marked for erasing, <b>BeginPaint</b> sends a <b>WM_ERASEBKGND</b> message to the window.

An application should not call <b>BeginPaint</b> except in response to a <b>WM_PAINT</b> message. Each call to <b>BeginPaint</b> must have a corresponding call to the <a href="/windows/desktop/api/winuser/nf-winuser-endpaint">EndPaint</a> function.

If the caret is in the area to be painted, <b>BeginPaint</b> automatically hides the caret to prevent it from being erased.

If the window's class has a background brush, <b>BeginPaint</b> uses that brush to erase the background of the update region before returning.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is always in terms of physical pixels.


#### Examples

For an example, see <a href="/windows/desktop/gdi/drawing-in-the-client-area">Drawing in the Client Area</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-endpaint">EndPaint</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidaterect">InvalidateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidatergn">InvalidateRgn</a>



<a href="/windows/desktop/api/winuser/ns-winuser-paintstruct">PAINTSTRUCT</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-validaterect">ValidateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-validatergn">ValidateRgn</a>
