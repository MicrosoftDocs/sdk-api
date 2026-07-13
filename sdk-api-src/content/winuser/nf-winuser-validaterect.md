---
UID: NF:winuser.ValidateRect
title: ValidateRect function (winuser.h)
description: The ValidateRect function validates the client area within a rectangle by removing the rectangle from the update region of the specified window.
helpviewer_keywords: ["ValidateRect","ValidateRect function [Windows GDI]","_win32_ValidateRect","gdi.validaterect","winuser/ValidateRect"]
old-location: gdi\validaterect.htm
tech.root: gdi
ms.assetid: 961dd768-1849-44df-bc7f-480881ed6477
ms.date: 12/05/2018
ms.keywords: ValidateRect, ValidateRect function [Windows GDI], _win32_ValidateRect, gdi.validaterect, winuser/ValidateRect
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
 - ValidateRect
 - winuser/ValidateRect
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
 - ValidateRect
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# ValidateRect function


## -description

The <b>ValidateRect</b> function validates the client area within a rectangle by removing the rectangle from the update region of the specified window.

## -parameters

### -param hWnd [in]

Handle to the window whose update region is to be modified. If this parameter is <b>NULL</b>, the system invalidates and redraws all windows and sends the <b>WM_ERASEBKGND</b> and <b>WM_NCPAINT</b> messages to the window procedure before the function returns.

### -param lpRect [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the client coordinates of the rectangle to be removed from the update region. If this parameter is <b>NULL</b>, the entire client area is removed.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> function automatically validates the entire client area. Neither the <b>ValidateRect</b> nor <a href="/windows/desktop/api/winuser/nf-winuser-validatergn">ValidateRgn</a> function should be called if a portion of the update region must be validated before the next <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message is generated.

The system continues to generate <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> messages until the current update region is validated.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidaterect">InvalidateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidatergn">InvalidateRgn</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/winuser/nf-winuser-validatergn">ValidateRgn</a>



<a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a>
