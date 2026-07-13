---
UID: NF:winuser.InvalidateRgn
title: InvalidateRgn function (winuser.h)
description: The InvalidateRgn function invalidates the client area within the specified region by adding it to the current update region of a window.
helpviewer_keywords: ["InvalidateRgn","InvalidateRgn function [Windows GDI]","_win32_InvalidateRgn","gdi.invalidatergn","winuser/InvalidateRgn"]
old-location: gdi\invalidatergn.htm
tech.root: gdi
ms.assetid: b5b44efe-8045-4e54-89f9-1766689a053d
ms.date: 12/05/2018
ms.keywords: InvalidateRgn, InvalidateRgn function [Windows GDI], _win32_InvalidateRgn, gdi.invalidatergn, winuser/InvalidateRgn
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
 - InvalidateRgn
 - winuser/InvalidateRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-0.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - InvalidateRgn
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# InvalidateRgn function


## -description

The <b>InvalidateRgn</b> function invalidates the client area within the specified region by adding it to the current update region of a window. The invalidated region, along with all other areas in the update region, is marked for painting when the next <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message occurs.

## -parameters

### -param hWnd [in]

A handle to the window with an update region that is to be modified.

### -param hRgn [in]

A handle to the region to be added to the update region. The region is assumed to have client coordinates. If this parameter is <b>NULL</b>, the entire client area is added to the update region.

### -param bErase [in]

Specifies whether the background within the update region should be erased when the update region is processed. If this parameter is <b>TRUE</b>, the background is erased when the <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> function is called. If the parameter is <b>FALSE</b>, the background remains unchanged.

## -returns

The return value is always nonzero.

## -remarks

Invalidated areas accumulate in the update region until the next <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message is processed or until the region is validated by using the <a href="/windows/desktop/api/winuser/nf-winuser-validaterect">ValidateRect</a> or <a href="/windows/desktop/api/winuser/nf-winuser-validatergn">ValidateRgn</a> function.

The system sends a <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message to a window whenever its update region is not empty and there are no other messages in the application queue for that window.

The specified region must have been created by using one of the region functions.

If the <i>bErase</i> parameter is <b>TRUE</b> for any part of the update region, the background in the entire region is erased, not just in the specified part.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidaterect">InvalidateRect</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-validaterect">ValidateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-validatergn">ValidateRgn</a>



<a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a>
