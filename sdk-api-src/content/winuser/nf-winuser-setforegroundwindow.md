---
UID: NF:winuser.SetForegroundWindow
title: SetForegroundWindow function (winuser.h)
description: Brings the thread that created the specified window into the foreground and activates the window.
helpviewer_keywords: ["SetForegroundWindow","SetForegroundWindow function [Windows and Messages]","_win32_SetForegroundWindow","_win32_setforegroundwindow_cpp","winmsg.setforegroundwindow","winui._win32_setforegroundwindow","winuser/SetForegroundWindow"]
old-location: winmsg\setforegroundwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setforegroundwindow.htm
ms.date: 12/05/2018
ms.keywords: SetForegroundWindow, SetForegroundWindow function [Windows and Messages], _win32_SetForegroundWindow, _win32_setforegroundwindow_cpp, winmsg.setforegroundwindow, winui._win32_setforegroundwindow, winuser/SetForegroundWindow
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
 - SetForegroundWindow
 - winuser/SetForegroundWindow
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
 - SetForegroundWindow
---

# SetForegroundWindow function


## -description

Brings the thread that created the specified window into the foreground and activates the window. Keyboard input is directed to the window, and various visual cues are changed for the user. The system assigns a slightly higher priority to the thread that created the foreground window than it does to other threads.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window that should be activated and brought to the foreground.

## -returns

Type: <b>BOOL</b>

If the window was brought to the foreground, the return value is nonzero.
                    
                    

If the window was not brought to the foreground, the return value is zero.

## -remarks



 The system restricts which processes can set the foreground window. A process can set the foreground window by calling **SetForegroundWindow** only if:

* At least one of the following conditions is true:
  * The calling process is the *foreground process* -
    the process that created the previous foreground window.
  * The calling process was started by the foreground process.
  * There is no foreground process.
  * The calling process received the last input event.
  * Either the foreground process or the calling process is being debugged.
* And all of the following conditions are true:
  * The calling process belongs to a desktop application,
    not a UWP app or a Windows Store app designed for Windows 8 or 8.1.
  * The foreground has not been locked by a previous call to
    [**LockSetForegroundWindow**](nf-winuser-locksetforegroundwindow.md).
  * The foreground lock time-out has expired (see
    [**SPI_GETFOREGROUNDLOCKTIMEOUT** in **SystemParametersInfo**](
    nf-winuser-systemparametersinfoa.md#SPI_GETFOREGROUNDLOCKTIMEOUT)).
  * No menus are active.

This is not an exhaustive list of conditions; processes may be be allowed
or denied the right to set the foreground window for reasons not given here.

An application cannot force a window to the foreground while the user is working with another window. Instead, Windows flashes the taskbar button of the window to notify the user.

A process that can set the foreground window can enable another process to set the foreground window by calling the [**AllowSetForegroundWindow**](nf-winuser-allowsetforegroundwindow.md) function. The process specified by <i>dwProcessId</i> loses the ability to set the foreground window the next time the user generates input, unless the input is directed at that process, or the next time a process calls <b>AllowSetForegroundWindow</b>, unless that process is specified. 

The foreground process can disable calls to <b>SetForegroundWindow</b> by calling the [**LockSetForegroundWindow**](nf-winuser-locksetforegroundwindow.md) function. 




## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow">AllowSetForegroundWindow</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-flashwindowex">FlashWindowEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getforegroundwindow">GetForegroundWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-locksetforegroundwindow">LockSetForegroundWindow</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setactivewindow">SetActiveWindow</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>