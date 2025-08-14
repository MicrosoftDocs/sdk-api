---
UID: NF:winuser.UpdateWindow
title: UpdateWindow function (winuser.h)
description: The UpdateWindow function updates the client area of the specified window by sending a WM_PAINT message to the window if the window's update region is not empty.
helpviewer_keywords: ["UpdateWindow","UpdateWindow function [Windows GDI]","_win32_UpdateWindow","gdi.updatewindow","winuser/UpdateWindow"]
old-location: gdi\updatewindow.htm
tech.root: gdi
ms.assetid: 51a50f1f-7b4d-4acd-83a0-1877f5181766
ms.date: 12/05/2018
ms.keywords: UpdateWindow, UpdateWindow function [Windows GDI], _win32_UpdateWindow, gdi.updatewindow, winuser/UpdateWindow
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
 - UpdateWindow
 - winuser/UpdateWindow
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
 - UpdateWindow
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# UpdateWindow function


## -description

The <b>UpdateWindow</b> function updates the client area of the specified window by sending a <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message to the window if the window's update region is not empty. The function sends a <b>WM_PAINT</b> message directly to the window procedure of the specified window, bypassing the application queue. If the update region is empty, no message is sent.

## -parameters

### -param hWnd [in]

Handle to the window to be updated.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-excludeupdatergn">ExcludeUpdateRgn</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getupdaterect">GetUpdateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getupdatergn">GetUpdateRgn</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidaterect">InvalidateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidatergn">InvalidateRgn</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a>
