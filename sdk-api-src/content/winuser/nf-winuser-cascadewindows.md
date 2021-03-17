---
UID: NF:winuser.CascadeWindows
title: CascadeWindows function (winuser.h)
description: Cascades the specified child windows of the specified parent window.
helpviewer_keywords: ["CascadeWindows","CascadeWindows function [Windows and Messages]","MDITILE_SKIPDISABLED","MDITILE_ZORDER","_win32_CascadeWindows","_win32_cascadewindows_cpp","winmsg.cascadewindows","winui._win32_cascadewindows","winuser/CascadeWindows"]
old-location: winmsg\cascadewindows.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\cascadewindows.htm
ms.date: 12/05/2018
ms.keywords: CascadeWindows, CascadeWindows function [Windows and Messages], MDITILE_SKIPDISABLED, MDITILE_ZORDER, _win32_CascadeWindows, _win32_cascadewindows_cpp, winmsg.cascadewindows, winui._win32_cascadewindows, winuser/CascadeWindows
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
 - CascadeWindows
 - winuser/CascadeWindows
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
 - CascadeWindows
---

# CascadeWindows function


## -description

Cascades the specified child windows of the specified parent window.

## -parameters

### -param hwndParent [in, optional]

Type: <b>HWND</b>

A handle to the parent window. If this parameter is <b>NULL</b>, the desktop window is assumed.

### -param wHow [in]

Type: <b>UINT</b>

A cascade flag. This parameter can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MDITILE_SKIPDISABLED"></a><a id="mditile_skipdisabled"></a><dl>
<dt><b>MDITILE_SKIPDISABLED</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Prevents disabled MDI child windows from being cascaded. 

</td>
</tr>
<tr>
<td width="40%"><a id="MDITILE_ZORDER"></a><a id="mditile_zorder"></a><dl>
<dt><b>MDITILE_ZORDER</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Arranges the windows in Z order. If this value is not specified, the windows are arranged using the order specified in the <i>lpKids</i> array. 

</td>
</tr>
</table>

### -param lpRect [in, optional]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a structure that specifies the rectangular area, in client coordinates, within which the windows are arranged. This parameter can be <b>NULL</b>, in which case the client area of the parent window is used.

### -param cKids [in]

Type: <b>UINT</b>

The number of elements in the array specified by the 
<i>lpKids</i> parameter. This parameter is ignored if <i>lpKids</i> is <b>NULL</b>.

### -param lpKids [in, optional]

Type: <b>const HWND*</b>

An array of handles to the child windows to arrange. If a specified child window is a top-level window with the style <b>WS_EX_TOPMOST</b> or <b>WS_EX_TOOLWINDOW</b>, the child window is not arranged. If this parameter is <b>NULL</b>, all child windows of the specified parent window (or of the desktop window) are arranged.

## -returns

Type: <b>WORD</b>

If the function succeeds, the return value is the number of windows arranged.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

By default, <b>CascadeWindows</b> arranges the windows in the order provided by the <i>lpKids</i> array, but preserves the <a href="/windows/desktop/winmsg/window-features">Z-Order</a>. If you specify the <b>MDITILE_ZORDER</b> flag, <b>CascadeWindows</b> arranges the windows in Z order. 

Calling <b>CascadeWindows</b> causes all maximized windows to be restored to their previous size.

## -see-also

<a href="/windows/desktop/winmsg/windows">Windows Overview</a>