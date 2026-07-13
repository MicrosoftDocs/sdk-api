---
UID: NF:winuser.ScreenToClient
title: ScreenToClient function (winuser.h)
description: The ScreenToClient function converts the screen coordinates of a specified point on the screen to client-area coordinates.
helpviewer_keywords: ["ScreenToClient","ScreenToClient function [Windows GDI]","_win32_ScreenToClient","gdi.screentoclient","winuser/ScreenToClient"]
old-location: gdi\screentoclient.htm
tech.root: gdi
ms.assetid: 5d3e65d1-e0c8-4063-b2e8-dd9f482d3378
ms.date: 12/05/2018
ms.keywords: ScreenToClient, ScreenToClient function [Windows GDI], _win32_ScreenToClient, gdi.screentoclient, winuser/ScreenToClient
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
 - ScreenToClient
 - winuser/ScreenToClient
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
 - ScreenToClient
req.apiset: ext-ms-win-ntuser-window-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# ScreenToClient function


## -description

The <b>ScreenToClient</b> function converts the screen coordinates of a specified point on the screen to client-area coordinates.

## -parameters

### -param hWnd [in]

A handle to the window whose client area will be used for the conversion.

### -param lpPoint

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that specifies the screen coordinates to be converted.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The function uses the window identified by the <i>hWnd</i> parameter and the screen coordinates given in the <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure to compute client coordinates. It then replaces the screen coordinates with the client coordinates. The new coordinates are relative to the upper-left corner of the specified window's client area.

The <b>ScreenToClient</b> function assumes the specified point is in screen coordinates.

All coordinates are in device units.

Do not use <b>ScreenToClient</b> when in a mirroring situation, that is, when changing from left-to-right layout to right-to-left layout. Instead, use <a href="/windows/desktop/api/winuser/nf-winuser-mapwindowpoints">MapWindowPoints</a>. For more information, see "Window Layout and Mirroring" in <a href="/windows/desktop/winmsg/window-features">Window Features</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-clienttoscreen">ClientToScreen</a>



<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-mapwindowpoints">MapWindowPoints</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>
