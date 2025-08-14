---
UID: NF:winuser.GetWindowPlacement
title: GetWindowPlacement function (winuser.h)
description: Retrieves the show state and the restored, minimized, and maximized positions of the specified window.
helpviewer_keywords: ["GetWindowPlacement","GetWindowPlacement function [Windows and Messages]","_win32_GetWindowPlacement","_win32_getwindowplacement_cpp","winmsg.getwindowplacement","winui._win32_getwindowplacement","winuser/GetWindowPlacement"]
old-location: winmsg\getwindowplacement.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowplacement.htm
ms.date: 12/05/2018
ms.keywords: GetWindowPlacement, GetWindowPlacement function [Windows and Messages], _win32_GetWindowPlacement, _win32_getwindowplacement_cpp, winmsg.getwindowplacement, winui._win32_getwindowplacement, winuser/GetWindowPlacement
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
 - GetWindowPlacement
 - winuser/GetWindowPlacement
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetWindowPlacement
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# GetWindowPlacement function


## -description

Retrieves the show state and the restored, minimized, and maximized positions of the specified window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window.

### -param lpwndpl [in, out]

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-windowplacement">WINDOWPLACEMENT</a>*</b>

A pointer to the <a href="/windows/desktop/api/winuser/ns-winuser-windowplacement">WINDOWPLACEMENT</a> structure that receives the show state and position information. Before calling <b>GetWindowPlacement</b>, set the <b>length</b> member to <code>sizeof(WINDOWPLACEMENT)</code>. <b>GetWindowPlacement</b> fails if <i>lpwndpl</i>-&gt; <i>length</i> is not set correctly.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>flags</b> member of <a href="/windows/desktop/api/winuser/ns-winuser-windowplacement">WINDOWPLACEMENT</a> retrieved by this function is always zero. If the window identified by the <i>hWnd</i> parameter is maximized, the <b>showCmd</b> member is SW_SHOWMAXIMIZED. If the window is minimized, <b>showCmd</b> is SW_SHOWMINIMIZED. Otherwise, it is SW_SHOWNORMAL. 

The <b>length</b> member of <a href="/windows/desktop/api/winuser/ns-winuser-windowplacement">WINDOWPLACEMENT</a> must be set to sizeof(<b>WINDOWPLACEMENT</b>). If this member is not set correctly, the function returns <b>FALSE</b>. For additional remarks on the proper use of window placement coordinates, see <b>WINDOWPLACEMENT</b>.

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowplacement">SetWindowPlacement</a>



<a href="/windows/desktop/api/winuser/ns-winuser-windowplacement">WINDOWPLACEMENT</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
