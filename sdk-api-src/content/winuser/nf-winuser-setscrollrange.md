---
UID: NF:winuser.SetScrollRange
title: SetScrollRange function (winuser.h)
description: The SetScrollRange function sets the minimum and maximum scroll box positions for the specified scroll bar.
helpviewer_keywords: ["SB_CTL","SB_HORZ","SB_VERT","SetScrollRange","SetScrollRange function [Windows Controls]","_win32_SetScrollRange","_win32_SetScrollRange_cpp","controls.SetScrollRange","controls._win32_SetScrollRange","winuser/SetScrollRange"]
old-location: controls\SetScrollRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\setscrollrange.htm
ms.date: 12/05/2018
ms.keywords: SB_CTL, SB_HORZ, SB_VERT, SetScrollRange, SetScrollRange function [Windows Controls], _win32_SetScrollRange, _win32_SetScrollRange_cpp, controls.SetScrollRange, controls._win32_SetScrollRange, winuser/SetScrollRange
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
 - SetScrollRange
 - winuser/SetScrollRange
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
 - SetScrollRange
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# SetScrollRange function


## -description

The <b>SetScrollRange</b> function sets the minimum and maximum scroll box positions for the specified scroll bar. 


<div class="alert"><b>Note</b>  The <b>SetScrollRange</b> function is provided for backward compatibility. New applications should use the <a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a> function.</div><div> </div>

## -parameters

### -param hWnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a scroll bar control or a window with a standard scroll bar, depending on the value of the 
					<i>nBar</i> parameter.

### -param nBar [in]

Type: <b>int</b>

Specifies the scroll bar to be set. This parameter can be one of the following values. 

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
Sets the range of a scroll bar control. The 
						<i>hwnd</i> parameter must be the handle to the scroll bar control.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Sets the range of a window's standard horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Sets the range of a window's standard vertical scroll bar.

</td>
</tr>
</table>

### -param nMinPos [in]

Type: <b>int</b>

Specifies the minimum scrolling position.

### -param nMaxPos [in]

Type: <b>int</b>

Specifies the maximum scrolling position.

### -param bRedraw [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether the scroll bar should be redrawn to reflect the change. If this parameter is <b>TRUE</b>, the scroll bar is redrawn. If it is <b>FALSE</b>, the scroll bar is not redrawn.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

You can use <b>SetScrollRange</b> to hide the scroll bar by setting 
				<i>nMinPos</i> and 
				<i>nMaxPos</i> to the same value. An application should not call the <b>SetScrollRange</b> function to hide a scroll bar while processing a scroll bar message. New applications should use the <a href="/windows/desktop/api/winuser/nf-winuser-showscrollbar">ShowScrollBar</a> function to hide the scroll bar. 

If the call to <b>SetScrollRange</b> immediately follows a call to the <a href="/windows/desktop/api/winuser/nf-winuser-setscrollpos">SetScrollPos</a> function, the 
				<i>bRedraw</i> parameter in <b>SetScrollPos</b> must be zero to prevent the scroll bar from being drawn twice. 

The default range for a standard scroll bar is 0 through 100. The default range for a scroll bar control is empty (both the 
				<i>nMinPos</i> and 
				<i>nMaxPos</i> parameter values are zero). The difference between the values specified by the 
				<i>nMinPos</i> and 
				<i>nMaxPos</i> parameters must not be greater than the value of MAXLONG. 

Because the messages that indicate scroll bar position, 
				<a href="/windows/desktop/Controls/wm-hscroll">WM_HSCROLL</a> and 
				<a href="/windows/desktop/Controls/wm-vscroll">WM_VSCROLL</a>, are limited to 16 bits of position data, applications that rely solely on those messages for position data have a practical maximum value of 65,535 for the <b>SetScrollRange</b> function's 
				<i>nMaxPos</i> parameter. 

However, because the <a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a>, <a href="/windows/desktop/api/winuser/nf-winuser-setscrollpos">SetScrollPos</a>, <b>SetScrollRange</b>, <a href="/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getscrollpos">GetScrollPos</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-getscrollrange">GetScrollRange</a> functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the 
				<a href="/windows/desktop/Controls/wm-hscroll">WM_HSCROLL</a> and 
				<a href="/windows/desktop/Controls/wm-vscroll">WM_VSCROLL</a> messages. See <b>GetScrollInfo</b> for a description of the technique. 

If the <i>nBar</i> parameter is SB_CTL and the window specified by the <i>hWnd</i> parameter is not a system scroll bar control, the system sends the <a href="/windows/desktop/Controls/sbm-setrange">SBM_SETRANGE</a> message to the window to set scroll bar information.  This allows <b>SetScrollRange</b> to operate on a custom control that mimics a scroll bar.  If the window does not handle the <b>SBM_SETRANGE</b> message, the <b>SetScrollRange</b> function fails.


#### Examples



For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Using the Owner-Display Clipboard Format</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getscrollpos">GetScrollPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getscrollrange">GetScrollRange</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setscrollpos">SetScrollPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-showscrollbar">ShowScrollBar</a>
