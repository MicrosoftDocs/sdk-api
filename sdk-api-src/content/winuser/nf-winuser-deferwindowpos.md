---
UID: NF:winuser.DeferWindowPos
title: DeferWindowPos function (winuser.h)
description: Updates the specified multiple-window position structure for the specified window.
helpviewer_keywords: ["DeferWindowPos","DeferWindowPos function [Windows and Messages]","HWND_BOTTOM","HWND_NOTOPMOST","HWND_TOP","HWND_TOPMOST","SWP_DRAWFRAME","SWP_FRAMECHANGED","SWP_HIDEWINDOW","SWP_NOACTIVATE","SWP_NOCOPYBITS","SWP_NOMOVE","SWP_NOOWNERZORDER","SWP_NOREDRAW","SWP_NOREPOSITION","SWP_NOSENDCHANGING","SWP_NOSIZE","SWP_NOZORDER","SWP_SHOWWINDOW","_win32_DeferWindowPos","_win32_deferwindowpos_cpp","winmsg.deferwindowpos","winui._win32_deferwindowpos","winuser/DeferWindowPos"]
old-location: winmsg\deferwindowpos.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\deferwindowpos.htm
ms.date: 12/05/2018
ms.keywords: DeferWindowPos, DeferWindowPos function [Windows and Messages], HWND_BOTTOM, HWND_NOTOPMOST, HWND_TOP, HWND_TOPMOST, SWP_DRAWFRAME, SWP_FRAMECHANGED, SWP_HIDEWINDOW, SWP_NOACTIVATE, SWP_NOCOPYBITS, SWP_NOMOVE, SWP_NOOWNERZORDER, SWP_NOREDRAW, SWP_NOREPOSITION, SWP_NOSENDCHANGING, SWP_NOSIZE, SWP_NOZORDER, SWP_SHOWWINDOW, _win32_DeferWindowPos, _win32_deferwindowpos_cpp, winmsg.deferwindowpos, winui._win32_deferwindowpos, winuser/DeferWindowPos
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
 - DeferWindowPos
 - winuser/DeferWindowPos
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
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - DeferWindowPos
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# DeferWindowPos function


## -description

Updates the specified multiple-window 
			– position structure for the specified window. The function then returns a handle to the updated structure. The <a href="/windows/desktop/api/winuser/nf-winuser-enddeferwindowpos">EndDeferWindowPos</a> function uses the information in this structure to change the position and size of a number of windows simultaneously. The <a href="/windows/desktop/api/winuser/nf-winuser-begindeferwindowpos">BeginDeferWindowPos</a> function creates the structure.

## -parameters

### -param hWinPosInfo [in]

Type: <b>HDWP</b>

A handle to a multiple-window 
					– position structure that contains size and position information for one or more windows. This structure is returned by <a href="/windows/desktop/api/winuser/nf-winuser-begindeferwindowpos">BeginDeferWindowPos</a> or by the most recent call to <b>DeferWindowPos</b>.

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window for which update information is stored in the structure. All windows in a multiple-window 
					– position structure must have the same parent.

### -param hWndInsertAfter [in, optional]

Type: <b>HWND</b>

A handle to the window that precedes the positioned window in the Z order. This parameter must be a window handle or one of the following values. This parameter is ignored if the <b>SWP_NOZORDER</b> flag is set in the <i>uFlags</i> parameter. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HWND_BOTTOM"></a><a id="hwnd_bottom"></a><dl>
<dt><b>HWND_BOTTOM</b></dt>
<dt>((HWND)1)</dt>
</dl>
</td>
<td width="60%">
Places the window at the bottom of the Z order. If the <i>hWnd</i> parameter identifies a topmost window, the window loses its topmost status and is placed at the bottom of all other windows.

</td>
</tr>
<tr>
<td width="40%"><a id="HWND_NOTOPMOST"></a><a id="hwnd_notopmost"></a><dl>
<dt><b>HWND_NOTOPMOST</b></dt>
<dt>((HWND)-2)</dt>
</dl>
</td>
<td width="60%">
Places the window above all non-topmost windows (that is, behind all topmost windows). This flag has no effect if the window is already a non-topmost window.

</td>
</tr>
<tr>
<td width="40%"><a id="HWND_TOP"></a><a id="hwnd_top"></a><dl>
<dt><b>HWND_TOP</b></dt>
<dt>((HWND)0)</dt>
</dl>
</td>
<td width="60%">
Places the window at the top of the Z order.

</td>
</tr>
<tr>
<td width="40%"><a id="HWND_TOPMOST"></a><a id="hwnd_topmost"></a><dl>
<dt><b>HWND_TOPMOST</b></dt>
<dt>((HWND)-1)</dt>
</dl>
</td>
<td width="60%">
Places the window above all non-topmost windows. The window maintains its topmost position even when it is deactivated.

</td>
</tr>
</table>

### -param x [in]

Type: <b>int</b>

The x-coordinate of the window's upper-left corner.

### -param y [in]

Type: <b>int</b>

The y-coordinate of the window's upper-left corner.

### -param cx [in]

Type: <b>int</b>

The window's new width, in pixels.

### -param cy [in]

Type: <b>int</b>

The window's new height, in pixels.

### -param uFlags [in]

Type: <b>UINT</b>

A combination of the following values that affect the size and position of the window. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
Sends a <a href="/windows/desktop/winmsg/wm-nccalcsize">WM_NCCALCSIZE</a> message to the window, even if the window's size is not being changed. If this flag is not specified, <b>WM_NCCALCSIZE</b> is sent only when the window's size is being changed.

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
Retains the current position (ignores the <i>x</i> and <i>y</i> parameters).

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
Prevents the window from receiving the <a href="/windows/desktop/winmsg/wm-windowposchanging">WM_WINDOWPOSCHANGING</a> message.

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

Type: <b>HDWP</b>

The return value identifies the updated multiple-window 
						– position structure. The handle returned by this function may differ from the handle passed to the function. The new handle that this function returns should be passed during the next call to the <b>DeferWindowPos</b> or <a href="/windows/desktop/api/winuser/nf-winuser-enddeferwindowpos">EndDeferWindowPos</a> function. 

If insufficient system resources are available for the function to succeed, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a call to <b>DeferWindowPos</b> fails, the application should abandon the window-positioning operation and not call <a href="/windows/desktop/api/winuser/nf-winuser-enddeferwindowpos">EndDeferWindowPos</a>. 

If <b>SWP_NOZORDER</b> is not specified, the system places the window identified by the <i>hWnd</i> parameter in the position following the window identified by the <i>hWndInsertAfter</i> parameter. If <i>hWndInsertAfter</i> is <b>NULL</b> or <b>HWND_TOP</b>, the system places the <i>hWnd</i> window at the top of the Z order. If <i>hWndInsertAfter</i> is set to <b>HWND_BOTTOM</b>, the system places the <i>hWnd</i> window at the bottom of the Z order. 

All coordinates for child windows are relative to the upper-left corner of the parent window's client area. 

A window can be made a topmost window either by setting <i>hWndInsertAfter</i> to the <b>HWND_TOPMOST</b> flag and ensuring that the <b>SWP_NOZORDER</b> flag is not set, or by setting the window's position in the Z order so that it is above any existing topmost windows. When a non-topmost window is made topmost, its owned windows are also made topmost. Its owners, however, are not changed. 

If neither the <b>SWP_NOACTIVATE</b> nor <b>SWP_NOZORDER</b> flag is specified (that is, when the application requests that a window be simultaneously activated and its position in the Z order changed), the value specified in <i>hWndInsertAfter</i> is used only in the following circumstances: 

<ul>
<li>Neither the <b>HWND_TOPMOST</b> nor <b>HWND_NOTOPMOST</b> flag is specified in <i>hWndInsertAfter</i>. </li>
<li>The window identified by <i>hWnd</i> is not the active window. </li>
</ul>
An application cannot activate an inactive window without also bringing it to the top of the Z order. An application can change an activated window's position in the Z order without restrictions, or it can activate a window and then move it to the top of the topmost or non-topmost windows. 

A topmost window is no longer topmost if it is repositioned to the bottom (<b>HWND_BOTTOM</b>) of the Z order or after any non-topmost window. When a topmost window is made non-topmost, its owners and its owned windows are also made non-topmost windows. 

A non-topmost window may own a topmost window, but not vice versa. Any window (for example, a dialog box) owned by a topmost window is itself made a topmost window to ensure that all owned windows stay above their owner.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-begindeferwindowpos">BeginDeferWindowPos</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-enddeferwindowpos">EndDeferWindowPos</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
