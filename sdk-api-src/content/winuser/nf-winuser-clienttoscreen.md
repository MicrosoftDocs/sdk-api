---
UID: NF:winuser.ClientToScreen
title: ClientToScreen function (winuser.h)
description: The ClientToScreen function converts the client-area coordinates of a specified point to screen coordinates.
helpviewer_keywords: ["ClientToScreen","ClientToScreen function [Windows GDI]","_win32_ClientToScreen","gdi.clienttoscreen","winuser/ClientToScreen"]
old-location: gdi\clienttoscreen.htm
tech.root: gdi
ms.assetid: 3b1e2699-7f5f-444d-9072-f2ca7c8fa511
ms.date: 12/05/2018
ms.keywords: ClientToScreen, ClientToScreen function [Windows GDI], _win32_ClientToScreen, gdi.clienttoscreen, winuser/ClientToScreen
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
 - ClientToScreen
 - winuser/ClientToScreen
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
 - user32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - ClientToScreen
req.apiset: ext-ms-win-ntuser-window-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# ClientToScreen function


## -description

The <b>ClientToScreen</b> function converts the client-area coordinates of a specified point to screen coordinates.

## -parameters

### -param hWnd [in]

A handle to the window whose client area is used for the conversion.

### -param lpPoint [in, out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that contains the client coordinates to be converted. The new screen coordinates are copied into this structure if the function succeeds.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>ClientToScreen</b> function replaces the client-area coordinates in the <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure with the screen coordinates. The screen coordinates are relative to the upper-left corner of the screen. Note, a screen-coordinate point that is above the window's client area has a negative y-coordinate. Similarly, a screen coordinate to the left of a client area has a negative x-coordinate.

All coordinates are device coordinates.


#### Examples

For an example, see "Drawing Lines with the Mouse" in <a href="/windows/desktop/inputdev/using-mouse-input">Using Mouse Input</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-mapwindowpoints">MapWindowPoints</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/winuser/nf-winuser-screentoclient">ScreenToClient</a>
