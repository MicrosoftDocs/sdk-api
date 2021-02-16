---
UID: NS:winuser.tagWINDOWPOS
title: WINDOWPOS (winuser.h)
description: Contains information about the size and position of a window.
helpviewer_keywords: ["*LPWINDOWPOS","*PWINDOWPOS","LPWINDOWPOS","LPWINDOWPOS structure pointer [Windows and Messages]","PWINDOWPOS","PWINDOWPOS structure pointer [Windows and Messages]","SWP_ NOOWNERZORDER","SWP_DRAWFRAME","SWP_FRAMECHANGED","SWP_HIDEWINDOW","SWP_NOACTIVATE","SWP_NOCOPYBITS","SWP_NOMOVE","SWP_NOREDRAW","SWP_NOREPOSITION","SWP_NOSENDCHANGING","SWP_NOSIZE","SWP_NOZORDER","SWP_SHOWWINDOW","WINDOWPOS","WINDOWPOS structure [Windows and Messages]","_win32_WINDOWPOS_str","_win32_windowpos_str_cpp","winmsg.windowpos","winui._win32_windowpos_str","winuser/LPWINDOWPOS","winuser/PWINDOWPOS","winuser/WINDOWPOS"]
old-location: winmsg\windowpos.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\windowpos.htm
ms.date: 12/05/2018
ms.keywords: '*LPWINDOWPOS, *PWINDOWPOS, LPWINDOWPOS, LPWINDOWPOS structure pointer [Windows and Messages], PWINDOWPOS, PWINDOWPOS structure pointer [Windows and Messages], SWP_ NOOWNERZORDER, SWP_DRAWFRAME, SWP_FRAMECHANGED, SWP_HIDEWINDOW, SWP_NOACTIVATE, SWP_NOCOPYBITS, SWP_NOMOVE, SWP_NOREDRAW, SWP_NOREPOSITION, SWP_NOSENDCHANGING, SWP_NOSIZE, SWP_NOZORDER, SWP_SHOWWINDOW, WINDOWPOS, WINDOWPOS structure [Windows and Messages], _win32_WINDOWPOS_str, _win32_windowpos_str_cpp, winmsg.windowpos, winui._win32_windowpos_str, winuser/LPWINDOWPOS, winuser/PWINDOWPOS, winuser/WINDOWPOS'
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
req.typenames: WINDOWPOS, *LPWINDOWPOS, *PWINDOWPOS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWINDOWPOS
 - winuser/tagWINDOWPOS
 - LPWINDOWPOS
 - winuser/LPWINDOWPOS
 - WINDOWPOS
 - winuser/WINDOWPOS
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
 - WINDOWPOS
---

# WINDOWPOS structure


## -description

Contains information about the size and position of a window.

## -struct-fields

### -field hwndInsertAfter

Type: <b>HWND</b>

The position of the window in Z order (front-to-back position). This member can be a handle to the window behind which this window is placed, or can be one of the special values listed with the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a> function.

### -field hwnd

Type: <b>HWND</b>

A handle to the window.

### -field x

Type: <b>int</b>

The position of the left edge of the window.

### -field y

Type: <b>int</b>

The position of the top edge of the window.

### -field cx

Type: <b>int</b>

The window width, in pixels.

### -field cy

Type: <b>int</b>

The window height, in pixels.

### -field flags

Type: <b>UINT</b>

The window position. This member can be one or more of the following values. 

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
Draws a frame (defined in the window's class description) around the window. Same as the <b>SWP_FRAMECHANGED</b> flag.

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
Does not activate the window. If this flag is not set, the window is activated and moved to the top of either the topmost or non-topmost group (depending on the setting of the 
						<b>hwndInsertAfter</b> member).

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
Retains the current position (ignores the 
						<b>x</b> and 
						<b>y</b> members).

</td>
</tr>
<tr>
<td width="40%"><a id="SWP__NOOWNERZORDER"></a><a id="swp__noownerzorder"></a><dl>
<dt><b>SWP_
NOOWNERZORDER</b></dt>
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
Does not change the owner window's position in the Z order. Same as the <b>SWP_NOOWNERZORDER</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOSENDCHANGING"></a><a id="swp_nosendchanging"></a><dl>
<dt><b>SWP_NOSENDCHANGING</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
Prevents the window from receiving the 
						<a href="/windows/desktop/winmsg/wm-windowposchanging">WM_WINDOWPOSCHANGING</a> message.

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOSIZE"></a><a id="swp_nosize"></a><dl>
<dt><b>SWP_NOSIZE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Retains the current size (ignores the 
						<b>cx</b> and 
						<b>cy</b> members).

</td>
</tr>
<tr>
<td width="40%"><a id="SWP_NOZORDER"></a><a id="swp_nozorder"></a><dl>
<dt><b>SWP_NOZORDER</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Retains the current Z order (ignores the 
						<b>hwndInsertAfter</b> member).

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

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-enddeferwindowpos">EndDeferWindowPos</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a>



<a href="/windows/desktop/winmsg/wm-nccalcsize">WM_NCCALCSIZE</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>