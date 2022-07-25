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
ms.custom: snippet-project
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
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
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

 The system restricts which processes can set the foreground window. A process can set the foreground window only if one of the following conditions is true:

				

<ul>
<li>The process is the foreground process.</li>
<li>The process was started by the foreground process.</li>
<li>The process received the last input event.</li>
<li>There is no foreground process.</li>
<li>The process is being debugged.</li>
<li>The foreground process is not a Modern Application or the Start Screen.</li>
<li>The foreground is not locked (see <a href="/windows/desktop/api/winuser/nf-winuser-locksetforegroundwindow">LockSetForegroundWindow</a>).</li>
<li>The foreground lock time-out has expired (see <b>SPI_GETFOREGROUNDLOCKTIMEOUT</b> in <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>).</li>
<li>No menus are active.</li>
</ul>
An application cannot force a window to the foreground while the user is working with another window. Instead, Windows flashes the taskbar button of the window to notify the user.

A process that can set the foreground window can enable another process to set the foreground window by calling the <a href="/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow">AllowSetForegroundWindow</a> function. The process specified by <i>dwProcessId</i> loses the ability to set the foreground window the next time the user generates input, unless the input is directed at that process, or the next time a process calls <b>AllowSetForegroundWindow</b>, unless that process is specified. 

The foreground process can disable calls to <b>SetForegroundWindow</b> by calling the <a href="/windows/desktop/api/winuser/nf-winuser-locksetforegroundwindow">LockSetForegroundWindow</a> function.

## Example

The following code example demonstrates the use of **SetForegroundWindow**

```cpp
// If the window is invisible we will show it and make it topmost without the
// foreground focus. If the window is visible it will also be made the
// topmost window without the foreground focus. If wParam is TRUE then
// for both cases the window will be forced into the foreground focus

if (uMsg == m_ShowStageMessage) {

    BOOL bVisible = IsWindowVisible(hwnd);
    SetWindowPos(hwnd, HWND_TOP, 0, 0, 0, 0,
                    SWP_NOMOVE | SWP_NOSIZE | SWP_SHOWWINDOW |
                    (bVisible ? SWP_NOACTIVATE : 0));

    // Should we bring the window to the foreground
    if (wParam == TRUE) {
        SetForegroundWindow(hwnd);
    }
    return (LRESULT) 1;
}
```

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
