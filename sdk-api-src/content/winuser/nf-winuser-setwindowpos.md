---
UID: NF:winuser.SetWindowPos
title: SetWindowPos function
author: windows-sdk-content
description: Changes the size, position, and Z order of a child, pop-up, or top-level window. These windows are ordered according to their appearance on the screen. The topmost window receives the highest rank and is the first window in the Z order.
old-location: winmsg\setwindowpos.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setwindowpos.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: HWND_BOTTOM, HWND_NOTOPMOST, HWND_TOP, HWND_TOPMOST, SWP_ASYNCWINDOWPOS, SWP_DEFERERASE, SWP_DRAWFRAME, SWP_FRAMECHANGED, SWP_HIDEWINDOW, SWP_NOACTIVATE, SWP_NOCOPYBITS, SWP_NOMOVE, SWP_NOOWNERZORDER, SWP_NOREDRAW, SWP_NOREPOSITION, SWP_NOSENDCHANGING, SWP_NOSIZE, SWP_NOZORDER, SWP_SHOWWINDOW, SetWindowPos, SetWindowPos function [Windows and Messages], _win32_SetWindowPos, _win32_setwindowpos_cpp, winmsg.setwindowpos, winui._win32_setwindowpos, winuser/SetWindowPos
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
 - SetWindowPos
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetWindowPos function


## -description


Changes the size, position, and Z order of a child, pop-up, or top-level window. These windows are ordered according to their appearance on the screen. The topmost window receives the highest rank and is the first window in the Z order.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window.


### -param hWndInsertAfter [in, optional]

Type: <b>HWND</b>

A handle to the window to precede the positioned window in the Z order. This parameter must be a window handle or one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HWND_BOTTOM"></a><a id="hwnd_bottom"></a><dl>
<dt><b>HWND_BOTTOM</b></dt>
<dt>(HWND)1</dt>
</dl>
</td>
<td width="60%">
Places the window at the bottom of the Z order. If the <i>hWnd</i> parameter identifies a topmost window, the window loses its topmost status and is placed at the bottom of all other windows.

</td>
</tr>
<tr>
<td width="40%"><a id="HWND_NOTOPMOST"></a><a id="hwnd_notopmost"></a><dl>
<dt><b>HWND_NOTOPMOST</b></dt>
<dt>(HWND)-2</dt>
</dl>
</td>
<td width="60%">
Places the window above all non-topmost windows (that is, behind all topmost windows). This flag has no effect if the window is already a non-topmost window.

</td>
</tr>
<tr>
<td width="40%"><a id="HWND_TOP"></a><a id="hwnd_top"></a><dl>
<dt><b>HWND_TOP</b></dt>
<dt>(HWND)0</dt>
</dl>
</td>
<td width="60%">
Places the window at the top of the Z order.

</td>
</tr>
<tr>
<td width="40%"><a id="HWND_TOPMOST"></a><a id="hwnd_topmost"></a><dl>
<dt><b>HWND_TOPMOST</b></dt>
<dt>(HWND)-1</dt>
</dl>
</td>
<td width="60%">
Places the window above all non-topmost windows. The window maintains its topmost position even when it is deactivated.

</td>
</tr>
</table>
 

For more information about how this parameter is used, see the following Remarks section.


### -param X [in]

Type: <b>int</b>

The new position of the left side of the window, in client coordinates. 


### -param Y [in]

Type: <b>int</b>

The new position of the top of the window, in client coordinates. 


### -param cx [in]

Type: <b>int</b>

The new width of the window, in pixels. 


### -param cy [in]

Type: <b>int</b>

The new height of the window, in pixels. 


### -param uFlags [in]

Type: <b>UINT</b>

The window sizing and positioning flags. This parameter can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SWP_ASYNCWINDOWPOS"></a><a id="swp_asyncwindowpos"></a><dl>
<dt><b>SWP_ASYNCWINDOWPOS</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
If the calling thread and the thread that owns the window are attached to different input queues, the system posts the request to the thread that owns the window. This prevents the calling thread from blocking its execution while other threads process the request. 

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_DEFERERASE"></a><a id="swp_defererase"></a><dl>
<dt><b>SWP_DEFERERASE</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
Prevents generation of the <a href="https://msdn.microsoft.com/4446be4e-e0b9-46ce-95b2-bea876348c25">WM_SYNCPAINT</a> message. 

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_DRAWFRAME"></a><a id="swp_drawframe"></a><dl>
<dt><b>SWP_DRAWFRAME</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Draws a frame (defined in the window's class description) around the window.

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_FRAMECHANGED"></a><a id="swp_framechanged"></a><dl>
<dt><b>SWP_FRAMECHANGED</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Applies new frame styles set using the <a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a> function. Sends a <a href="https://msdn.microsoft.com/d2d5825e-02a5-44b8-8615-55b7259d24ba">WM_NCCALCSIZE</a> message to the window, even if the window's size is not being changed. If this flag is not specified, <b>WM_NCCALCSIZE</b> is sent only when the window's size is being changed.

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_HIDEWINDOW"></a><a id="swp_hidewindow"></a><dl>
<dt><b>SWP_HIDEWINDOW</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Hides the window.

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOACTIVATE"></a><a id="swp_noactivate"></a><dl>
<dt><b>SWP_NOACTIVATE</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Does not activate the window. If this flag is not set, the window is activated and moved to the top of either the topmost or non-topmost group (depending on the setting of the <i>hWndInsertAfter</i> parameter).

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOCOPYBITS"></a><a id="swp_nocopybits"></a><dl>
<dt><b>SWP_NOCOPYBITS</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Discards the entire contents of the client area. If this flag is not specified, the valid contents of the client area are saved and copied back into the client area after the window is sized or repositioned.

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOMOVE"></a><a id="swp_nomove"></a><dl>
<dt><b>SWP_NOMOVE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Retains the current position (ignores <i>X</i> and <i>Y</i> parameters).

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOOWNERZORDER"></a><a id="swp_noownerzorder"></a><dl>
<dt><b>SWP_NOOWNERZORDER</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Does not change the owner window's position in the Z order.

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOREDRAW"></a><a id="swp_noredraw"></a><dl>
<dt><b>SWP_NOREDRAW</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Does not redraw changes. If this flag is set, no repainting of any kind occurs. This applies to the client area, the nonclient area (including the title bar and scroll bars), and any part of the parent window uncovered as a result of the window being moved. When this flag is set, the application must explicitly invalidate or redraw any parts of the window and parent window that need redrawing.

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOREPOSITION"></a><a id="swp_noreposition"></a><dl>
<dt><b>SWP_NOREPOSITION</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Same as the <b>SWP_NOOWNERZORDER</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOSENDCHANGING"></a><a id="swp_nosendchanging"></a><dl>
<dt><b>SWP_NOSENDCHANGING</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
Prevents the window from receiving the <a href="https://msdn.microsoft.com/45ecd966-5222-4738-9e99-8a6edbdd435a">WM_WINDOWPOSCHANGING</a> message.

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOSIZE"></a><a id="swp_nosize"></a><dl>
<dt><b>SWP_NOSIZE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Retains the current size (ignores the <i>cx</i> and <i>cy</i> parameters).

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOZORDER"></a><a id="swp_nozorder"></a><dl>
<dt><b>SWP_NOZORDER</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Retains the current Z order (ignores the <i>hWndInsertAfter</i> parameter).

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_SHOWWINDOW"></a><a id="swp_showwindow"></a><dl>
<dt><b>SWP_SHOWWINDOW</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Displays the window.

</td>
</tr>
</table>
 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



As part of the Vista re-architecture, all services were moved off the interactive desktop into Session 0. hwnd and window manager operations are only effective inside a session and cross-session attempts to manipulate the hwnd will fail. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=204865">The Windows Vista Developer Story: Application Compatibility Cookbook</a>.

If you have changed certain window data using <a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a>, you must call <b>SetWindowPos</b> for the changes to take effect. Use the following combination for <i>uFlags</i>: <code>SWP_NOMOVE | SWP_NOSIZE | SWP_NOZORDER | SWP_FRAMECHANGED</code>. 

A window can be made a topmost window either by setting the <i>hWndInsertAfter</i> parameter to <b>HWND_TOPMOST</b> and ensuring that the <b>SWP_NOZORDER</b> flag is not set, or by setting a window's position in the Z order so that it is above any existing topmost windows. When a non-topmost window is made topmost, its owned windows are also made topmost. Its owners, however, are not changed. 

If neither the <b>SWP_NOACTIVATE</b> nor <b>SWP_NOZORDER</b> flag is specified (that is, when the application requests that a window be simultaneously activated and its position in the Z order changed), the value specified in <i>hWndInsertAfter</i> is used only in the following circumstances. 

<ul>
<li>Neither the <b>HWND_TOPMOST</b> nor <b>HWND_NOTOPMOST</b> flag is specified in <i>hWndInsertAfter</i>. </li>
<li>The window identified by <i>hWnd</i> is not the active window. </li>
</ul>
An application cannot activate an inactive window without also bringing it to the top of the Z order. Applications can change an activated window's position in the Z order without restrictions, or it can activate a window and then move it to the top of the topmost or non-topmost windows. 

If a topmost window is repositioned to the bottom (<b>HWND_BOTTOM</b>) of the Z order or after any non-topmost window, it is no longer topmost. When a topmost window is made non-topmost, its owners and its owned windows are also made non-topmost windows. 

A non-topmost window can own a topmost window, but the reverse cannot occur. Any window (for example, a dialog box) owned by a topmost window is itself made a topmost window, to ensure that all owned windows stay above their owner. 

If an application is not in the foreground, and should be in the foreground, it must call the <a href="https://msdn.microsoft.com/c728ff42-1a5e-45c9-b2ab-5e28ad430a2d">SetForegroundWindow</a> function. 

To use <b>SetWindowPos</b> to bring a window to the top, the process that owns the window must have <a href="https://msdn.microsoft.com/c728ff42-1a5e-45c9-b2ab-5e28ad430a2d">SetForegroundWindow</a> permission. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/8a5b6bdd-4429-4f48-b846-6bd617a87abf">Initializing a Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b844d1a8-a417-43d5-87da-9869990deea4">MoveWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/3a761bd3-5eba-4263-b670-405d91996a89">SetActiveWindow</a>



<a href="https://msdn.microsoft.com/c728ff42-1a5e-45c9-b2ab-5e28ad430a2d">SetForegroundWindow</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

