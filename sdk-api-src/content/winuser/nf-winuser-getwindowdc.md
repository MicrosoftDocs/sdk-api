---
UID: NF:winuser.GetWindowDC
title: GetWindowDC function (winuser.h)
description: The GetWindowDC function retrieves the device context (DC) for the entire window, including title bar, menus, and scroll bars.
helpviewer_keywords: ["GetWindowDC","GetWindowDC function [Windows GDI]","_win32_GetWindowDC","gdi.getwindowdc","winuser/GetWindowDC"]
old-location: gdi\getwindowdc.htm
tech.root: gdi
ms.assetid: 9e6a135e-e337-4129-a3ad-faf9a8ac9b2d
ms.date: 12/05/2018
ms.keywords: GetWindowDC, GetWindowDC function [Windows GDI], _win32_GetWindowDC, gdi.getwindowdc, winuser/GetWindowDC
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
 - GetWindowDC
 - winuser/GetWindowDC
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
 - GetWindowDC
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# GetWindowDC function


## -description

The <b>GetWindowDC</b> function retrieves the device context (DC) for the entire window, including title bar, menus, and scroll bars. A window device context permits painting anywhere in a window, because the origin of the device context is the upper-left corner of the window instead of the client area.

<b>GetWindowDC</b> assigns default attributes to the window device context each time it retrieves the device context. Previous attributes are lost.

## -parameters

### -param hWnd [in]

A handle to the window with a device context that is to be retrieved. If this value is <b>NULL</b>, <b>GetWindowDC</b> retrieves the device context for the entire screen.

If this parameter is <b>NULL</b>, <b>GetWindowDC</b> retrieves the device context for the primary display monitor. To get the device context for other display monitors, use the <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a> functions.

## -returns

If the function succeeds, the return value is a handle to a device context for the specified window.

If the function fails, the return value is <b>NULL</b>, indicating an error or an invalid <i>hWnd</i> parameter.

## -remarks

<b>GetWindowDC</b> is intended for special painting effects within a window's nonclient area. Painting in nonclient areas of any window is not recommended.

The <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> function can be used to retrieve the dimensions of various parts of the nonclient area, such as the title bar, menu, and scroll bars.

The <a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a> function can be used to retrieve a device context for the entire screen.

After painting is complete, the <a href="/windows/desktop/api/winuser/nf-winuser-releasedc">ReleaseDC</a> function must be called to release the device context. Not releasing the window device context has serious effects on painting requested by applications.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-releasedc">ReleaseDC</a>
