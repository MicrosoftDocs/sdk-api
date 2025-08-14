---
UID: NF:winuser.WindowFromPoint
title: WindowFromPoint function (winuser.h)
description: Retrieves a handle to the window that contains the specified point.
helpviewer_keywords: ["WindowFromPoint","WindowFromPoint function [Windows and Messages]","_win32_WindowFromPoint","_win32_windowfrompoint_cpp","winmsg.windowfrompoint","winui._win32_windowfrompoint","winuser/WindowFromPoint"]
old-location: winmsg\windowfrompoint.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\windowfrompoint.htm
ms.date: 12/05/2018
ms.keywords: WindowFromPoint, WindowFromPoint function [Windows and Messages], _win32_WindowFromPoint, _win32_windowfrompoint_cpp, winmsg.windowfrompoint, winui._win32_windowfrompoint, winuser/WindowFromPoint
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
 - WindowFromPoint
 - winuser/WindowFromPoint
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
 - WindowFromPoint
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# WindowFromPoint function


## -description

Retrieves a handle to the window that contains the specified point.

## -parameters

### -param Point [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The point to be checked.

## -returns

Type: <b>HWND</b>

The return value is a handle to the window that contains the point. If no window exists at the given point, the return value is <b>NULL</b>. If the point is over a static text control, the return value is a handle to the window under the static text control.

## -remarks

The <b>WindowFromPoint</b> function does not retrieve a handle to a hidden or disabled window, even if the point is within the window. An application should use the <a href="/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint">ChildWindowFromPoint</a> function for a nonrestrictive search. 


#### Examples

For an example, see "Interface from Running Object Table" in <a href="/windows/desktop/Controls/about-text-object-model">About Text Object Model</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint">ChildWindowFromPoint</a>



<b>Conceptual</b>



<b>Other Resources</b>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-windowfromdc">WindowFromDC</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
