---
UID: NF:winuser.GetScrollPos
title: GetScrollPos function (winuser.h)
description: The GetScrollPos function retrieves the current position of the scroll box (thumb) in the specified scroll bar.
helpviewer_keywords: ["GetScrollPos","GetScrollPos function [Windows Controls]","SB_CTL","SB_HORZ","SB_VERT","_win32_GetScrollPos","_win32_GetScrollPos_cpp","controls.GetScrollPos","controls._win32_GetScrollPos","winuser/GetScrollPos"]
old-location: controls\GetScrollPos.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\getscrollpos.htm
ms.date: 12/05/2018
ms.keywords: GetScrollPos, GetScrollPos function [Windows Controls], SB_CTL, SB_HORZ, SB_VERT, _win32_GetScrollPos, _win32_GetScrollPos_cpp, controls.GetScrollPos, controls._win32_GetScrollPos, winuser/GetScrollPos
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
 - GetScrollPos
 - winuser/GetScrollPos
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
 - GetScrollPos
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# GetScrollPos function


## -description

The <b>GetScrollPos</b> function retrieves the current position of the scroll box (thumb) in the specified scroll bar. The current position is a relative value that depends on the current scrolling range. For example, if the scrolling range is 0 through 100 and the scroll box is in the middle of the bar, the current position is 50.

			
<div class="alert"><b>Note</b>   The <b>GetScrollPos</b> function is provided for backward compatibility. New applications should use the <a href="/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a> function. </div><div> </div>

## -parameters

### -param hWnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a scroll bar control or a window with a standard scroll bar, depending on the value of the 
					<i>nBar</i> parameter.

### -param nBar [in]

Type: <b>int</b>

Specifies the scroll bar to be examined. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SB_CTL"></a><a id="sb_ctl"></a><dl>
<dt><b>SB_CTL</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the position of the scroll box in a scroll bar control. The 
						<i>hWnd</i> parameter must be the handle to the scroll bar control.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the position of the scroll box in a window's standard horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the position of the scroll box in a window's standard vertical scroll bar.

</td>
</tr>
</table>

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the current position of the scroll box.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>GetScrollPos</b> function enables applications to use 32-bit scroll positions. Although the messages that indicate scroll bar position, <a href="/windows/desktop/Controls/wm-hscroll">WM_HSCROLL</a> and <a href="/windows/desktop/Controls/wm-vscroll">WM_VSCROLL</a>, are limited to 16 bits of position data, the functions <a href="/windows/desktop/api/winuser/nf-winuser-setscrollpos">SetScrollPos</a>, <a href="/windows/desktop/api/winuser/nf-winuser-setscrollrange">SetScrollRange</a>, <b>GetScrollPos</b>, and <a href="/windows/desktop/api/winuser/nf-winuser-getscrollrange">GetScrollRange</a> support 32-bit scroll bar position data. Thus, an application can call <b>GetScrollPos</b> while processing either the <b>WM_HSCROLL</b> or <b>WM_VSCROLL</b> messages to obtain 32-bit scroll bar position data. 

To get the 32-bit position of the scroll box (thumb) during a SB_THUMBTRACK request code in a <a href="/windows/desktop/Controls/wm-hscroll">WM_HSCROLL</a> or <a href="/windows/desktop/Controls/wm-vscroll">WM_VSCROLL</a> message, use the <a href="/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a> function.

If the <i>nBar</i> parameter is SB_CTL and the window specified by the <i>hWnd</i> parameter is not a system scroll bar control, the system sends the <a href="/windows/desktop/Controls/sbm-getpos">SBM_GETPOS</a> message to the window to obtain scroll bar information.  This allows <b>GetScrollPos</b> to operate on a custom control that mimics a scroll bar.  If the window does not handle the <b>SBM_GETPOS</b> message, the <b>GetScrollPos</b> function fails.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getscrollrange">GetScrollRange</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setscrollpos">SetScrollPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setscrollrange">SetScrollRange</a>



<a href="/windows/desktop/Controls/wm-hscroll">WM_HSCROLL</a>



<a href="/windows/desktop/Controls/wm-vscroll">WM_VSCROLL</a>
