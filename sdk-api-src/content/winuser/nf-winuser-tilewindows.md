---
UID: NF:winuser.TileWindows
title: TileWindows function (winuser.h)
description: Tiles the specified child windows of the specified parent window.
helpviewer_keywords: ["MDITILE_HORIZONTAL","MDITILE_VERTICAL","TileWindows","TileWindows function [Windows and Messages]","_win32_TileWindows","_win32_tilewindows_cpp","winmsg.tilewindows","winui._win32_tilewindows","winuser/TileWindows"]
old-location: winmsg\tilewindows.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\tilewindows.htm
ms.date: 12/05/2018
ms.keywords: MDITILE_HORIZONTAL, MDITILE_VERTICAL, TileWindows, TileWindows function [Windows and Messages], _win32_TileWindows, _win32_tilewindows_cpp, winmsg.tilewindows, winui._win32_tilewindows, winuser/TileWindows
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
 - TileWindows
 - winuser/TileWindows
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - TileWindows
---

# TileWindows function


## -description

Tiles the specified child windows of the specified parent window.

## -parameters

### -param hwndParent [in, optional]

Type: <b>HWND</b>

A handle to the parent window. If this parameter is <b>NULL</b>, the desktop window is assumed.

### -param wHow [in]

Type: <b>UINT</b>

The tiling flags. This parameter can be one of the following values—optionally combined with <b>MDITILE_SKIPDISABLED</b> to prevent disabled MDI child windows from being tiled. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MDITILE_HORIZONTAL"></a><a id="mditile_horizontal"></a><dl>
<dt><b>MDITILE_HORIZONTAL</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Tiles windows horizontally.

</td>
</tr>
<tr>
<td width="40%"><a id="MDITILE_VERTICAL"></a><a id="mditile_vertical"></a><dl>
<dt><b>MDITILE_VERTICAL</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Tiles windows vertically.

</td>
</tr>
</table>

### -param lpRect [in, optional]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a structure that specifies the rectangular area, in client coordinates, within which the windows are arranged. If this parameter is <b>NULL</b>, the client area of the parent window is used.

### -param cKids [in]

Type: <b>UINT</b>

The number of elements in the array specified by the <i>lpKids</i> parameter. This parameter is ignored if <i>lpKids</i> is <b>NULL</b>.

### -param lpKids [in, optional]

Type: <b>const HWND*</b>

An array of handles to the child windows to arrange. If a specified child window is a top-level window with the style <b>WS_EX_TOPMOST</b> or <b>WS_EX_TOOLWINDOW</b>, the child window is not arranged. If this parameter is <b>NULL</b>, all child windows of the specified parent window (or of the desktop window) are arranged.

## -returns

Type: <b>WORD</b>

If the function succeeds, the return value is the number of windows arranged.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Calling <b>TileWindows</b> causes all maximized windows to be restored to their previous size.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-cascadewindows">CascadeWindows</a>



<b>Conceptual</b>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>