---
UID: NF:winuser.IsWindowVisible
title: IsWindowVisible function (winuser.h)
description: Determines the visibility state of the specified window.
helpviewer_keywords: ["IsWindowVisible","IsWindowVisible function [Windows and Messages]","_win32_IsWindowVisible","_win32_iswindowvisible_cpp","winmsg.iswindowvisible","winui._win32_iswindowvisible","winuser/IsWindowVisible"]
old-location: winmsg\iswindowvisible.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\iswindowvisible.htm
ms.date: 12/05/2018
ms.keywords: IsWindowVisible, IsWindowVisible function [Windows and Messages], _win32_IsWindowVisible, _win32_iswindowvisible_cpp, winmsg.iswindowvisible, winui._win32_iswindowvisible, winuser/IsWindowVisible
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
 - IsWindowVisible
 - winuser/IsWindowVisible
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
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsWindowVisible
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# IsWindowVisible function


## -description

Determines the visibility state of the specified window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be tested.

## -returns

Type: <b>BOOL</b>

If the specified window, its parent window, its parent's parent window, and so forth, have the <b>WS_VISIBLE</b> style, the return value is nonzero. Otherwise, the return value is zero. 

Because the return value specifies whether the window has the <b>WS_VISIBLE</b> style, it may be nonzero even if the window is totally obscured by other windows.

## -remarks

The visibility state of a window is indicated by the <b>WS_VISIBLE</b> style bit. When <b>WS_VISIBLE</b> is set, the window is displayed and subsequent drawing into it is displayed as long as the window has the <b>WS_VISIBLE</b> style. 

Any drawing to a window with the <b>WS_VISIBLE</b> style will not be displayed if the window is obscured by other windows or is clipped by its parent window.

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
