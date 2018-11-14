---
UID: NF:winuser.ShowWindow
title: ShowWindow function
author: windows-sdk-content
description: Sets the specified window's show state.
old-location: winmsg\showwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\showwindow.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SW_FORCEMINIMIZE, SW_HIDE, SW_MAXIMIZE, SW_MINIMIZE, SW_RESTORE, SW_SHOW, SW_SHOWDEFAULT, SW_SHOWMAXIMIZED, SW_SHOWMINIMIZED, SW_SHOWMINNOACTIVE, SW_SHOWNA, SW_SHOWNOACTIVATE, SW_SHOWNORMAL, ShowWindow, ShowWindow function [Windows and Messages], _win32_ShowWindow, _win32_showwindow_cpp, winmsg.showwindow, winui._win32_showwindow, winuser/ShowWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - ShowWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ShowWindow
: 
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

Controls how the window is to be shown. This parameter is ignored the first time an application calls <b>ShowWindow</b>, if the program that launched the application provides a <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure. Otherwise, the first time <b>ShowWindow</b> is called, the value should be the value obtained by the <a href="https://msdn.microsoft.com/e704ccb6-b4ab-4e1b-8d25-2209de3d38f8">WinMain</a> function in its <i>nCmdShow</i> parameter. In subsequent calls, this parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SW_FORCEMINIMIZE"></a><a id="sw_forceminimize"></a><dl>
<dt><b>SW_FORCEMINIMIZE</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Minimizes a window, even if the thread that owns the window is not responding. This flag should only be used when minimizing windows from a different thread.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_HIDE"></a><a id="sw_hide"></a><dl>
<dt><b>SW_HIDE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Hides the window and activates another window.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_MAXIMIZE"></a><a id="sw_maximize"></a><dl>
<dt><b>SW_MAXIMIZE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Maximizes the specified window.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_MINIMIZE"></a><a id="sw_minimize"></a><dl>
<dt><b>SW_MINIMIZE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Minimizes the specified window and activates the next top-level window in the Z order.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_RESTORE"></a><a id="sw_restore"></a><dl>
<dt><b>SW_RESTORE</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Activates and displays the window. If the window is minimized or maximized, the system restores it to its original size and position. An application should specify this flag when restoring a minimized window.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOW"></a><a id="sw_show"></a><dl>
<dt><b>SW_SHOW</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Activates the window and displays it in its current size and position. 

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWDEFAULT"></a><a id="sw_showdefault"></a><dl>
<dt><b>SW_SHOWDEFAULT</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Sets the show state based on the SW_ value specified in the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure passed to the <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function by the program that started the application. 

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWMAXIMIZED"></a><a id="sw_showmaximized"></a><dl>
<dt><b>SW_SHOWMAXIMIZED</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Activates the window and displays it as a maximized window.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWMINIMIZED"></a><a id="sw_showminimized"></a><dl>
<dt><b>SW_SHOWMINIMIZED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Activates the window and displays it as a minimized window.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWMINNOACTIVE"></a><a id="sw_showminnoactive"></a><dl>
<dt><b>SW_SHOWMINNOACTIVE</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Displays the window as a minimized window. This value is similar to <b>SW_SHOWMINIMIZED</b>, except the window is not activated.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWNA"></a><a id="sw_showna"></a><dl>
<dt><b>SW_SHOWNA</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Displays the window in its current size and position. This value is similar to <b>SW_SHOW</b>, except that the window is not activated.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWNOACTIVATE"></a><a id="sw_shownoactivate"></a><dl>
<dt><b>SW_SHOWNOACTIVATE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Displays a window in its most recent size and position. This value is similar to <b>SW_SHOWNORMAL</b>, except that the window is not activated.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWNORMAL"></a><a id="sw_shownormal"></a><dl>
<dt><b>SW_SHOWNORMAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Activates and displays a window. If the window is minimized or maximized, the system restores it to its original size and position. An application should specify this flag when displaying the window for the first time.

</td>
</tr>
</table>
 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the window was previously visible, the return value is nonzero. 

If the window was previously hidden, the return value is zero. 




## -remarks



To perform certain special effects when showing or hiding a window, use <a href="https://msdn.microsoft.com/b10a4dfd-d544-41de-b359-4946e4030560">AnimateWindow</a>. 

The first time an application calls <b>ShowWindow</b>, it should use the <a href="https://msdn.microsoft.com/e704ccb6-b4ab-4e1b-8d25-2209de3d38f8">WinMain</a> function's <i>nCmdShow</i> parameter as its <i>nCmdShow</i> parameter. Subsequent calls to <b>ShowWindow</b> must use one of the values in the given list, instead of the one specified by the <b>WinMain</b> function's <i>nCmdShow</i> parameter. 

As noted in the discussion of the <i>nCmdShow</i> parameter, the <i>nCmdShow</i> value is ignored in the first call to <b>ShowWindow</b> if the program that launched the application specifies startup information in the  structure. In this case, <b>ShowWindow</b> uses the information specified in the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure to show the window. On subsequent calls, the application must call <b>ShowWindow</b> with <i>nCmdShow</i> set to <b>SW_SHOWDEFAULT</b> to use the startup information provided by the program that launched the application. This behavior is designed for the following situations: 

<ul>
<li>Applications create their main window by calling <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> with the <b>WS_VISIBLE</b> flag set. </li>
<li>Applications create their main window by calling <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> with the <b>WS_VISIBLE</b> flag cleared, and later call <b>ShowWindow</b> with the <b>SW_SHOW</b> flag set to make it visible. </li>
</ul>

#### Examples

For an example, see <a href="using_windows.htm">Creating a Main Window</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b10a4dfd-d544-41de-b359-4946e4030560">AnimateWindow</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a>



<a href="https://msdn.microsoft.com/ca4cd67b-6db1-43a9-8918-1400fef2ea1e">ShowOwnedPopups</a>



<a href="https://msdn.microsoft.com/ecc6ceb6-78af-4be5-9639-7f1e286d24c3">ShowWindowAsync</a>



<a href="https://msdn.microsoft.com/e704ccb6-b4ab-4e1b-8d25-2209de3d38f8">WinMain</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

