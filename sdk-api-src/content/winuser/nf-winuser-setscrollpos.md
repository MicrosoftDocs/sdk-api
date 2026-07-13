---
UID: NF:winuser.SetScrollPos
title: SetScrollPos function (winuser.h)
description: The SetScrollPos function sets the position of the scroll box (thumb) in the specified scroll bar and, if requested, redraws the scroll bar to reflect the new position of the scroll box.
helpviewer_keywords: ["SB_CTL","SB_HORZ","SB_VERT","SetScrollPos","SetScrollPos function [Windows Controls]","_win32_SetScrollPos","_win32_SetScrollPos_cpp","controls.SetScrollPos","controls._win32_SetScrollPos","winuser/SetScrollPos"]
old-location: controls\SetScrollPos.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\setscrollpos.htm
ms.date: 12/05/2018
ms.keywords: SB_CTL, SB_HORZ, SB_VERT, SetScrollPos, SetScrollPos function [Windows Controls], _win32_SetScrollPos, _win32_SetScrollPos_cpp, controls.SetScrollPos, controls._win32_SetScrollPos, winuser/SetScrollPos
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
 - SetScrollPos
 - winuser/SetScrollPos
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
 - SetScrollPos
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# SetScrollPos function


## -description

The <b>SetScrollPos</b> function sets the position of the scroll box (thumb) in the specified scroll bar and, if requested, redraws the scroll bar to reflect the new position of the scroll box.

        
<div class="alert"><b>Note</b>  The <b>SetScrollPos</b> function is provided for backward compatibility. New applications should use the <a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a> function.</div><div> </div>

## -parameters

### -param hWnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a scroll bar control or a window with a standard scroll bar, depending on the value of the <i>nBar</i> parameter.

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
Sets the position of the scroll box in a scroll bar control. The <i>hwnd</i> parameter must be the handle to the scroll bar control.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Sets the position of the scroll box in a window's standard horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Sets the position of the scroll box in a window's standard vertical scroll bar.

</td>
</tr>
</table>

### -param nPos [in]

Type: <b>int</b>

Specifies the new position of the scroll box. The position must be within the scrolling range. For more information about the scrolling range, see the <a href="/windows/desktop/api/winuser/nf-winuser-setscrollrange">SetScrollRange</a> function.

### -param bRedraw [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether the scroll bar is redrawn to reflect the new scroll box position. If this parameter is <b>TRUE</b>, the scroll bar is redrawn. If it is <b>FALSE</b>, the scroll bar is not redrawn.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the previous position of the scroll box.
                    
                    

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the scroll bar is redrawn by a subsequent call to another function, setting the <i>bRedraw</i> parameter to <b>FALSE</b> is useful. 

Because the messages that indicate scroll bar position, <a href="/windows/desktop/Controls/wm-hscroll">WM_HSCROLL</a> and <a href="/windows/desktop/Controls/wm-vscroll">WM_VSCROLL</a>, are limited to 16 bits of position data, applications that rely solely on those messages for position data have a practical maximum value of 65,535 for the <b>SetScrollPos</b> function's <i>nPos</i> parameter. 

However, because the <a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a>, <b>SetScrollPos</b>, <a href="/windows/desktop/api/winuser/nf-winuser-setscrollrange">SetScrollRange</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getscrollpos">GetScrollPos</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-getscrollrange">GetScrollRange</a> functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the <a href="/windows/desktop/Controls/wm-hscroll">WM_HSCROLL</a> and <a href="/windows/desktop/Controls/wm-vscroll">WM_VSCROLL</a> messages. See <b>GetScrollInfo</b> for a description of the technique. 

If the <i>nBar</i> parameter is SB_CTL and the window specified by the <i>hWnd</i> parameter is not a system scroll bar control, the system sends the <a href="/windows/desktop/Controls/sbm-setpos">SBM_SETPOS</a> message to the window to set scroll bar information.  This allows <b>SetScrollPos</b> to operate on a custom control that mimics a scroll bar.  If the window does not handle the <b>SBM_SETPOS</b> message, the <b>SetScrollPos</b> function fails.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getscrollpos">GetScrollPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getscrollrange">GetScrollRange</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setscrollrange">SetScrollRange</a>
