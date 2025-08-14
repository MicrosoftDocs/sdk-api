---
UID: NF:winuser.ShowScrollBar
title: ShowScrollBar function (winuser.h)
description: The ShowScrollBar function shows or hides the specified scroll bar.
helpviewer_keywords: ["SB_BOTH","SB_CTL","SB_HORZ","SB_VERT","ShowScrollBar","ShowScrollBar function [Windows Controls]","_win32_ShowScrollBar","_win32_ShowScrollBar_cpp","controls.ShowScrollBar","controls._win32_ShowScrollBar","winuser/ShowScrollBar"]
old-location: controls\ShowScrollBar.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\showscrollbar.htm
ms.date: 12/05/2018
ms.keywords: SB_BOTH, SB_CTL, SB_HORZ, SB_VERT, ShowScrollBar, ShowScrollBar function [Windows Controls], _win32_ShowScrollBar, _win32_ShowScrollBar_cpp, controls.ShowScrollBar, controls._win32_ShowScrollBar, winuser/ShowScrollBar
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ShowScrollBar
 - winuser/ShowScrollBar
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - ShowScrollBar
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# ShowScrollBar function


## -description

The <b>ShowScrollBar</b> function shows or hides the specified scroll bar.

## -parameters

### -param hWnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a scroll bar control or a window with a standard scroll bar, depending on the value of the 
					<i>wBar</i> parameter.

### -param wBar [in]

Type: <b>int</b>

Specifies the scroll bar(s) to be shown or hidden. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SB_BOTH"></a><a id="sb_both"></a><dl>
<dt><b>SB_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Shows or hides a window's standard horizontal and vertical scroll bars.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_CTL"></a><a id="sb_ctl"></a><dl>
<dt><b>SB_CTL</b></dt>
</dl>
</td>
<td width="60%">
Shows or hides a scroll bar control. The 
						<i>hwnd</i> parameter must be the handle to the scroll bar control.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Shows or hides a window's standard horizontal scroll bars.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Shows or hides a window's standard vertical scroll bar.

</td>
</tr>
</table>

### -param bShow [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether the scroll bar is shown or hidden. If this parameter is <b>TRUE</b>, the scroll bar is shown; otherwise, it is hidden.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

You should not call this function to hide a scroll bar while processing a scroll bar message.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-enablescrollbar">EnableScrollBar</a>
