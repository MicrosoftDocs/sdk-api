---
UID: NS:winuser.tagWINDOWPLACEMENT
title: tagWINDOWPLACEMENT
author: windows-sdk-content
description: Contains information about the placement of a window on the screen.
old-location: winmsg\windowplacement.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\windowplacement.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PWINDOWPLACEMENT, LPWINDOWPLACEMENT, LPWINDOWPLACEMENT structure pointer [Windows and Messages], PWINDOWPLACEMENT, PWINDOWPLACEMENT structure pointer [Windows and Messages], SW_HIDE, SW_MAXIMIZE, SW_MINIMIZE, SW_RESTORE, SW_SHOW, SW_SHOWMAXIMIZED, SW_SHOWMINIMIZED, SW_SHOWMINNOACTIVE, SW_SHOWNA, SW_SHOWNOACTIVATE, SW_SHOWNORMAL, WINDOWPLACEMENT, WINDOWPLACEMENT structure [Windows and Messages], WPF_ASYNCWINDOWPLACEMENT, WPF_RESTORETOMAXIMIZED, WPF_SETMINPOSITION, _win32_WINDOWPLACEMENT_str, _win32_windowplacement_str_cpp, tagWINDOWPLACEMENT, winmsg.windowplacement, winui._win32_windowplacement_str, winuser/LPWINDOWPLACEMENT, winuser/PWINDOWPLACEMENT, winuser/WINDOWPLACEMENT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - WINDOWPLACEMENT
product: Windows
targetos: Windows
req.typenames: WINDOWPLACEMENT
req.redist: 
---

# tagWINDOWPLACEMENT structure


## -description


Contains information about the placement of a window on the screen. 


## -struct-fields




### -field length

Type: <b>UINT</b>

The length of the structure, in bytes. Before calling the <a href="https://msdn.microsoft.com/en-us/library/ms633518(v=VS.85).aspx">GetWindowPlacement</a> or <a href="https://msdn.microsoft.com/en-us/library/ms633544(v=VS.85).aspx">SetWindowPlacement</a> functions, set this member to <code>sizeof(WINDOWPLACEMENT)</code>. 
                    


<a href="https://msdn.microsoft.com/en-us/library/ms633518(v=VS.85).aspx">GetWindowPlacement</a> and <a href="https://msdn.microsoft.com/en-us/library/ms633544(v=VS.85).aspx">SetWindowPlacement</a> fail if this member is not set correctly.


### -field flags

Type: <b>UINT</b>

The flags that control the position of the minimized window and the method by which the window is restored. This member can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WPF_ASYNCWINDOWPLACEMENT"></a><a id="wpf_asyncwindowplacement"></a><dl>
<dt><b>WPF_ASYNCWINDOWPLACEMENT</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
 If the calling thread and the thread that owns the window are attached to different input queues, the system posts the request to the thread that owns the window. This prevents the calling thread from blocking its execution while other threads process the request.

</td>
</tr>
<tr>
<td width="40%"><a id="WPF_RESTORETOMAXIMIZED"></a><a id="wpf_restoretomaximized"></a><dl>
<dt><b>WPF_RESTORETOMAXIMIZED</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The restored window will be maximized, regardless of whether it was maximized before it was minimized. This setting is only valid the next time the window is restored. It does not change the default restoration behavior. 
                        

This flag is only valid when the <b>SW_SHOWMINIMIZED</b> value is specified for the <b>showCmd</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="WPF_SETMINPOSITION"></a><a id="wpf_setminposition"></a><dl>
<dt><b>WPF_SETMINPOSITION</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The coordinates of the minimized window may be specified. 
                        

This flag must be specified if the coordinates are set in the <b>ptMinPosition</b> member.

</td>
</tr>
</table>
 


### -field showCmd

Type: <b>UINT</b>

The current show state of the window. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
Minimizes the specified window and activates the next top-level window in the z-order.

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
Displays the window as a minimized window. 
                        

This value is similar to <b>SW_SHOWMINIMIZED</b>, except the window is not activated.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWNA"></a><a id="sw_showna"></a><dl>
<dt><b>SW_SHOWNA</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Displays the window in its current size and position. 
                        

This value is similar to <b>SW_SHOW</b>, except the window is not activated.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWNOACTIVATE"></a><a id="sw_shownoactivate"></a><dl>
<dt><b>SW_SHOWNOACTIVATE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Displays a window in its most recent size and position. 
                        

This value is similar to <b>SW_SHOWNORMAL</b>, except the window is not activated.

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
 


### -field ptMinPosition

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

The coordinates of the window's upper-left corner when the window is minimized. 


### -field ptMaxPosition

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

The coordinates of the window's upper-left corner when the window is maximized. 


### -field rcNormalPosition

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

The window's coordinates when the window is in the restored position. 


### -field rcDevice

 




## -remarks



If the window is a top-level window that does not have the <b>WS_EX_TOOLWINDOW</b> window style, then the coordinates represented by the following members are in workspace coordinates: <b>ptMinPosition</b>, <b>ptMaxPosition</b>, and <b>rcNormalPosition</b>. Otherwise, these members are in screen coordinates.

Workspace coordinates differ from screen coordinates in that they take the locations and sizes of application toolbars (including the taskbar) into account. Workspace coordinate (0,0) is the upper-left corner of the workspace area, the area of the screen not being used by application toolbars.

The coordinates used in a <b>WINDOWPLACEMENT</b> structure should be used only by the <a href="https://msdn.microsoft.com/en-us/library/ms633518(v=VS.85).aspx">GetWindowPlacement</a> and <a href="https://msdn.microsoft.com/en-us/library/ms633544(v=VS.85).aspx">SetWindowPlacement</a> functions. Passing workspace coordinates to functions which expect screen coordinates (such as <a href="https://msdn.microsoft.com/en-us/library/ms633545(v=VS.85).aspx">SetWindowPos</a>) will result in the window appearing in the wrong location. For example, if the taskbar is at the top of the screen, saving window coordinates using <b>GetWindowPlacement</b> and restoring them using <b>SetWindowPos</b> causes the window to appear to "creep" up the screen. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633518(v=VS.85).aspx">GetWindowPlacement</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633544(v=VS.85).aspx">SetWindowPlacement</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633545(v=VS.85).aspx">SetWindowPos</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633548(v=VS.85).aspx">ShowWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

