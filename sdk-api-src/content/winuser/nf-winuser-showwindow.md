---
UID: NF:winuser.ShowWindow
title: ShowWindow function (winuser.h)
description: Sets the specified window's show state.
helpviewer_keywords: ["SW_FORCEMINIMIZE","SW_HIDE","SW_MAXIMIZE","SW_MINIMIZE","SW_RESTORE","SW_SHOW","SW_SHOWDEFAULT","SW_SHOWMAXIMIZED","SW_SHOWMINIMIZED","SW_SHOWMINNOACTIVE","SW_SHOWNA","SW_SHOWNOACTIVATE","SW_SHOWNORMAL","ShowWindow","ShowWindow function [Windows and Messages]","_win32_ShowWindow","_win32_showwindow_cpp","winmsg.showwindow","winui._win32_showwindow","winuser/ShowWindow"]
old-location: winmsg\showwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\showwindow.htm
ms.date: 06/06/2023
ms.keywords: SW_FORCEMINIMIZE, SW_HIDE, SW_MAXIMIZE, SW_MINIMIZE, SW_RESTORE, SW_SHOW, SW_SHOWDEFAULT, SW_SHOWMAXIMIZED, SW_SHOWMINIMIZED, SW_SHOWMINNOACTIVE, SW_SHOWNA, SW_SHOWNOACTIVATE, SW_SHOWNORMAL, ShowWindow, ShowWindow function [Windows and Messages], _win32_ShowWindow, _win32_showwindow_cpp, winmsg.showwindow, winui._win32_showwindow, winuser/ShowWindow
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
 - ShowWindow
 - winuser/ShowWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-l1-1-0.dll
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
 - ShowWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# ShowWindow function


## -description

Sets the specified window's show state.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window.

### -param nCmdShow [in]

Type: <b>int</b>

Controls how the window is to be shown. This parameter is ignored the first time an application calls <b>ShowWindow</b>, if the program that launched the application provides a <a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure. Otherwise, the first time <b>ShowWindow</b> is called, the value should be the value obtained by the <a href="/windows/desktop/api/winbase/nf-winbase-winmain">WinMain</a> function in its <i>nCmdShow</i> parameter. In subsequent calls, this parameter can be one of the following values. 

| Value | Meaning |
|-------|---------|
| **SW\_HIDE**<br>0 | Hides the window and activates another window. |
| **SW\_SHOWNORMAL**<br>**SW\_NORMAL**<br>1 | Activates and displays a window. If the window is minimized, maximized, or arranged, the system restores it to its original size and position. An application should specify this flag when displaying the window for the first time. |
| **SW\_SHOWMINIMIZED**<br>2 | Activates the window and displays it as a minimized window. |
| **SW\_SHOWMAXIMIZED**<br>**SW\_MAXIMIZE**<br>3 | Activates the window and displays it as a maximized window. |
| **SW\_SHOWNOACTIVATE**<br>4 | Displays a window in its most recent size and position. This value is similar to **SW_SHOWNORMAL**, except that the window is not activated. |
| **SW\_SHOW**<br>5 | Activates the window and displays it in its current size and position. |
| **SW\_MINIMIZE**<br>6 | Minimizes the specified window and activates the next top-level window in the Z order. |
| **SW\_SHOWMINNOACTIVE**<br>7 | Displays the window as a minimized window. This value is similar to **SW_SHOWMINIMIZED**, except the window is not activated. |
| **SW\_SHOWNA**<br>8 | Displays the window in its current size and position. This value is similar to **SW\_SHOW**, except that the window is not activated. |
| **SW\_RESTORE**<br>9 | Activates and displays the window. If the window is minimized, maximized, or arranged, the system restores it to its original size and position. An application should specify this flag when restoring a minimized window. |
| **SW\_SHOWDEFAULT**<br>10 | Sets the show state based on the **SW\_** value specified in the [STARTUPINFO](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure passed to the [CreateProcess](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function by the program that started the application. |
| **SW\_FORCEMINIMIZE**<br>11 | Minimizes a window, even if the thread that owns the window is not responding. This flag should only be used when minimizing windows from a different thread. |

## -returns

Type: <b>BOOL</b>

If the window was previously visible, the return value is nonzero. 

If the window was previously hidden, the return value is zero.

## -remarks

To perform certain special effects when showing or hiding a window, use <a href="/windows/desktop/api/winuser/nf-winuser-animatewindow">AnimateWindow</a>. 

The first time an application calls <b>ShowWindow</b>, it should use the <a href="/windows/desktop/api/winbase/nf-winbase-winmain">WinMain</a> function's <i>nCmdShow</i> parameter as its <i>nCmdShow</i> parameter. Subsequent calls to <b>ShowWindow</b> must use one of the values in the given list, instead of the one specified by the <b>WinMain</b> function's <i>nCmdShow</i> parameter. 

As noted in the discussion of the <i>nCmdShow</i> parameter, the <i>nCmdShow</i> value is ignored in the first call to <b>ShowWindow</b> if the program that launched the application specifies startup information in the  structure. In this case, <b>ShowWindow</b> uses the information specified in the <a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure to show the window. On subsequent calls, the application must call <b>ShowWindow</b> with <i>nCmdShow</i> set to <b>SW_SHOWDEFAULT</b> to use the startup information provided by the program that launched the application. This behavior is designed for the following situations: 

<ul>
<li>Applications create their main window by calling <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> with the <b>WS_VISIBLE</b> flag set. </li>
<li>Applications create their main window by calling <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> with the <b>WS_VISIBLE</b> flag cleared, and later call <b>ShowWindow</b> with the <b>SW_SHOW</b> flag set to make it visible. </li>
</ul>

#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-windows">Creating a Main Window</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-animatewindow">AnimateWindow</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a>



<a href="/windows/desktop/api/winuser/nf-winuser-showownedpopups">ShowOwnedPopups</a>



<a href="/windows/desktop/api/winuser/nf-winuser-showwindowasync">ShowWindowAsync</a>



<a href="/windows/desktop/api/winbase/nf-winbase-winmain">WinMain</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
