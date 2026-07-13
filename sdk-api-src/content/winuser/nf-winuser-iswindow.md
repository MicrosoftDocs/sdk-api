---
UID: NF:winuser.IsWindow
title: IsWindow function (winuser.h)
description: Determines whether the specified window handle identifies an existing window.
helpviewer_keywords: ["IsWindow","IsWindow function [Windows and Messages]","_win32_IsWindow","_win32_iswindow_cpp","winmsg.iswindow","winui._win32_iswindow","winuser/IsWindow"]
old-location: winmsg\iswindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\iswindow.htm
ms.date: 12/05/2018
ms.keywords: IsWindow, IsWindow function [Windows and Messages], _win32_IsWindow, _win32_iswindow_cpp, winmsg.iswindow, winui._win32_iswindow, winuser/IsWindow
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
 - IsWindow
 - winuser/IsWindow
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
 - IsWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# IsWindow function


## -description

Determines whether the specified window handle identifies an existing window.

## -parameters

### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window to be tested.

## -returns

Type: <b>BOOL</b>

If the window handle identifies an existing window, the return value is nonzero.

If the window handle does not identify an existing window, the return value is zero.

## -remarks

A thread should not use <b>IsWindow</b> for a window that it did not create because the window could be destroyed after this function was called. Further, because window handles are recycled the handle could even point to a different window. 


#### Examples

For an example, see <a href="/windows/desktop/dlgbox/using-dialog-boxes">Creating a Modeless Dialog Box</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-iswindowenabled">IsWindowEnabled</a>



<a href="/windows/desktop/api/winuser/nf-winuser-iswindowvisible">IsWindowVisible</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
