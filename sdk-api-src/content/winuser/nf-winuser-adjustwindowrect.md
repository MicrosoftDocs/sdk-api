---
UID: NF:winuser.AdjustWindowRect
title: AdjustWindowRect function (winuser.h)
description: Calculates the required size of the window rectangle, based on the desired client-rectangle size. The window rectangle can then be passed to the CreateWindow function to create a window whose client area is the desired size.
helpviewer_keywords: ["AdjustWindowRect","AdjustWindowRect function [Windows and Messages]","_win32_AdjustWindowRect","_win32_adjustwindowrect_cpp","winmsg.adjustwindowrect","winui._win32_adjustwindowrect","winuser/AdjustWindowRect"]
old-location: winmsg\adjustwindowrect.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\adjustwindowrect.htm
ms.date: 12/05/2018
ms.keywords: AdjustWindowRect, AdjustWindowRect function [Windows and Messages], _win32_AdjustWindowRect, _win32_adjustwindowrect_cpp, winmsg.adjustwindowrect, winui._win32_adjustwindowrect, winuser/AdjustWindowRect
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
 - AdjustWindowRect
 - winuser/AdjustWindowRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
api_name:
 - AdjustWindowRect
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# AdjustWindowRect function


## -description

Calculates the required size of the window rectangle, based on the desired client-rectangle size. The window rectangle can then be passed to the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> function to create a window whose client area is the desired size.

To specify an extended window style, use the <a href="/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex">AdjustWindowRectEx</a> function.

## -parameters

### -param lpRect [in, out]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the coordinates of the top-left and bottom-right corners of the desired client area. When the function returns, the structure contains the coordinates of the top-left and bottom-right corners of the window to accommodate the desired client area.

### -param dwStyle [in]

Type: <b>DWORD</b>

The <a href="/windows/desktop/winmsg/window-styles">window style</a> of the window whose required size is to be calculated. Note that you cannot specify the <b>WS_OVERLAPPED</b> style.

### -param bMenu [in]

Type: <b>BOOL</b>

Indicates whether the window has a menu.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A client rectangle is the smallest rectangle that completely encloses a client area. A window rectangle is the smallest rectangle that completely encloses the window, which includes the client area and the nonclient area. 

The <b>AdjustWindowRect</b> function does not add extra space when a menu bar wraps to two or more rows. 

The <b>AdjustWindowRect</b> function does not take the <b>WS_VSCROLL</b> or <b>WS_HSCROLL</b> styles into account. To account for the scroll bars, call the  <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> function with <b>SM_CXVSCROLL</b> or <b>SM_CYHSCROLL</b>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex">AdjustWindowRectEx</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
