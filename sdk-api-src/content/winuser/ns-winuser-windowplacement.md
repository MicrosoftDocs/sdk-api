---
UID: NS:winuser.tagWINDOWPLACEMENT
title: WINDOWPLACEMENT (winuser.h)
description: Contains information about the placement of a window on the screen.
helpviewer_keywords: ["*PWINDOWPLACEMENT","LPWINDOWPLACEMENT","LPWINDOWPLACEMENT structure pointer [Windows and Messages]","PWINDOWPLACEMENT","PWINDOWPLACEMENT structure pointer [Windows and Messages]","WINDOWPLACEMENT","WINDOWPLACEMENT structure [Windows and Messages]","WPF_ASYNCWINDOWPLACEMENT","WPF_RESTORETOMAXIMIZED","WPF_SETMINPOSITION","_win32_WINDOWPLACEMENT_str","_win32_windowplacement_str_cpp","winmsg.windowplacement","winui._win32_windowplacement_str","winuser/LPWINDOWPLACEMENT","winuser/PWINDOWPLACEMENT","winuser/WINDOWPLACEMENT"]
old-location: winmsg\windowplacement.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\windowplacement.htm
ms.date: 12/05/2018
ms.keywords: '*PWINDOWPLACEMENT, LPWINDOWPLACEMENT, LPWINDOWPLACEMENT structure pointer [Windows and Messages], PWINDOWPLACEMENT, PWINDOWPLACEMENT structure pointer [Windows and Messages], SW_HIDE, SW_MAXIMIZE, SW_MINIMIZE, SW_RESTORE, SW_SHOW, SW_SHOWMAXIMIZED, SW_SHOWMINIMIZED, SW_SHOWMINNOACTIVE, SW_SHOWNA, SW_SHOWNOACTIVATE, SW_SHOWNORMAL, WINDOWPLACEMENT, WINDOWPLACEMENT structure [Windows and Messages], WPF_ASYNCWINDOWPLACEMENT, WPF_RESTORETOMAXIMIZED, WPF_SETMINPOSITION, _win32_WINDOWPLACEMENT_str, _win32_windowplacement_str_cpp, winmsg.windowplacement, winui._win32_windowplacement_str, winuser/LPWINDOWPLACEMENT, winuser/PWINDOWPLACEMENT, winuser/WINDOWPLACEMENT'
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
targetos: Windows
req.typenames: WINDOWPLACEMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWINDOWPLACEMENT
 - winuser/tagWINDOWPLACEMENT
 - WINDOWPLACEMENT
 - winuser/WINDOWPLACEMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - WINDOWPLACEMENT
---

# WINDOWPLACEMENT structure


## -description

Contains information about the placement of a window on the screen.

## -struct-fields

### -field length

Type: <b>UINT</b>

The length of the structure, in bytes. Before calling the <a href="/windows/desktop/api/winuser/nf-winuser-getwindowplacement">GetWindowPlacement</a> or <a href="/windows/desktop/api/winuser/nf-winuser-setwindowplacement">SetWindowPlacement</a> functions, set this member to <code>sizeof(WINDOWPLACEMENT)</code>. 
                    


<a href="/windows/desktop/api/winuser/nf-winuser-getwindowplacement">GetWindowPlacement</a> and <a href="/windows/desktop/api/winuser/nf-winuser-setwindowplacement">SetWindowPlacement</a> fail if this member is not set correctly.

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

The current show state of the window. It can be any of the values that can be specified in the <i>nCmdShow</i> parameter for the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function.

### -field ptMinPosition

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The coordinates of the window's upper-left corner when the window is minimized.

### -field ptMaxPosition

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The coordinates of the window's upper-left corner when the window is maximized.

### -field rcNormalPosition

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The window's coordinates when the window is in the restored position.

### -field rcDevice

## -remarks

If the window is a top-level window that does not have the <b>WS_EX_TOOLWINDOW</b> window style, then the coordinates represented by the following members are in workspace coordinates: <b>ptMinPosition</b>, <b>ptMaxPosition</b>, and <b>rcNormalPosition</b>. Otherwise, these members are in screen coordinates.

Workspace coordinates differ from screen coordinates in that they take the locations and sizes of application toolbars (including the taskbar) into account. Workspace coordinate (0,0) is the upper-left corner of the workspace area, the area of the screen not being used by application toolbars.

The coordinates used in a <b>WINDOWPLACEMENT</b> structure should be used only by the <a href="/windows/desktop/api/winuser/nf-winuser-getwindowplacement">GetWindowPlacement</a> and <a href="/windows/desktop/api/winuser/nf-winuser-setwindowplacement">SetWindowPlacement</a> functions. Passing workspace coordinates to functions which expect screen coordinates (such as <a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a>) will result in the window appearing in the wrong location. For example, if the taskbar is at the top of the screen, saving window coordinates using <b>GetWindowPlacement</b> and restoring them using <b>SetWindowPos</b> causes the window to appear to "creep" up the screen.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowplacement">GetWindowPlacement</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowplacement">SetWindowPlacement</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>