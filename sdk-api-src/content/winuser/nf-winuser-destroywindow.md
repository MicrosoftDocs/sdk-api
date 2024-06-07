---
UID: NF:winuser.DestroyWindow
title: DestroyWindow function (winuser.h)
description: Destroys the specified window.
helpviewer_keywords: ["DestroyWindow","DestroyWindow function [Windows and Messages]","_win32_DestroyWindow","_win32_destroywindow_cpp","winmsg.destroywindow","winui._win32_destroywindow","winuser/DestroyWindow"]
old-location: winmsg\destroywindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\destroywindow.htm
ms.date: 12/05/2018
ms.keywords: DestroyWindow, DestroyWindow function [Windows and Messages], _win32_DestroyWindow, _win32_destroywindow_cpp, winmsg.destroywindow, winui._win32_destroywindow, winuser/DestroyWindow
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
 - DestroyWindow
 - winuser/DestroyWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
 - DestroyWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# DestroyWindow function


## -description

Destroys the specified window. The function sends <a href="/windows/desktop/winmsg/wm-destroy">WM_DESTROY</a> and <a href="/windows/desktop/winmsg/wm-ncdestroy">WM_NCDESTROY</a> messages to the window to deactivate it and remove the keyboard focus from it. The function also destroys the window's menu, destroys timers, removes clipboard ownership, and breaks the clipboard viewer chain (if the window is at the top of the viewer chain).

If the specified window is a parent or owner window, <b>DestroyWindow</b> automatically destroys the associated child or owned windows when it destroys the parent or owner window. The function first destroys child or owned windows, and then it destroys the parent or owner window.

<b>DestroyWindow</b> also destroys modeless dialog boxes created by the <a href="/windows/desktop/api/winuser/nf-winuser-createdialoga">CreateDialog</a> function.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be destroyed.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A thread cannot use <b>DestroyWindow</b> to destroy a window created by a different thread. 

If the window being destroyed is a child window that does not have the <b>WS_EX_NOPARENTNOTIFY</b> style, a <a href="/windows/win32/inputmsg/wm-parentnotify">WM_PARENTNOTIFY</a> message is sent to the parent. 


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-windows">Destroying a Window</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialoga">CreateDialog</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-destroy">WM_DESTROY</a>



<a href="/windows/desktop/winmsg/wm-ncdestroy">WM_NCDESTROY</a>



<a href="/windows/win32/inputmsg/wm-parentnotify">WM_PARENTNOTIFY</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
