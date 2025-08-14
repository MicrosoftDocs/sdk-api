---
UID: NF:winuser.GetWindowRect
title: GetWindowRect function (winuser.h)
description: Retrieves the dimensions of the bounding rectangle of the specified window. The dimensions are given in screen coordinates that are relative to the upper-left corner of the screen.
helpviewer_keywords: ["GetWindowRect","GetWindowRect function [Windows and Messages]","_win32_GetWindowRect","_win32_getwindowrect_cpp","winmsg.getwindowrect","winui._win32_getwindowrect","winuser/GetWindowRect"]
old-location: winmsg\getwindowrect.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowrect.htm
ms.date: 12/05/2018
ms.keywords: GetWindowRect, GetWindowRect function [Windows and Messages], _win32_GetWindowRect, _win32_getwindowrect_cpp, winmsg.getwindowrect, winui._win32_getwindowrect, winuser/GetWindowRect
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
 - GetWindowRect
 - winuser/GetWindowRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetWindowRect
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# GetWindowRect function


## -description

Retrieves the dimensions of the bounding rectangle of the specified window. The dimensions are given in screen coordinates that are relative to the upper-left corner of the screen.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window.

### -param lpRect [out]

Type: <b>LPRECT</b>

A pointer to a  <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the screen coordinates of the upper-left and lower-right corners of the window.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

In conformance with conventions for the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure, the bottom-right coordinates of the returned rectangle are exclusive. In other words, the pixel at (<b>right</b>, <b>bottom</b>) lies immediately outside the rectangle.

GetWindowRect is virtualized for DPI.

In Windows Vista and later, the Window Rect now may include invisible resize borders.

To get the visible window bounds, not including the invisible resize borders,
use <a href="/windows/win32/api/dwmapi/nf-dwmapi-dwmgetwindowattribute">DwmGetWindowAttribute</a>,
specifying <b>DWMWA_EXTENDED_FRAME_BOUNDS</b>. Note that unlike the Window Rect,
the DWM Extended Frame Bounds are not adjusted for DPI.

#### Examples

For an example, see <a href="/windows/desktop/dlgbox/using-dialog-boxes">Initializing a Dialog Box</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getclientrect">GetClientRect</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-screentoclient">ScreenToClient</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
