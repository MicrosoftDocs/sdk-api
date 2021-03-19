---
UID: NF:commctrl.FlatSB_SetScrollInfo
title: FlatSB_SetScrollInfo function (commctrl.h)
description: Sets the information for a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard SetScrollInfo function.
helpviewer_keywords: ["FlatSB_SetScrollInfo","FlatSB_SetScrollInfo function [Windows Controls]","SB_HORZ","SB_VERT","SIF_ALL","SIF_DISABLENOSCROLL","SIF_PAGE","SIF_POS","SIF_RANGE","_win32_FlatSB_SetScrollInfo","_win32_FlatSB_SetScrollInfo_cpp","commctrl/FlatSB_SetScrollInfo","controls.FlatSB_SetScrollInfo","controls._win32_FlatSB_SetScrollInfo"]
old-location: controls\FlatSB_SetScrollInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\flatsb_setscrollinfo.htm
ms.date: 12/05/2018
ms.keywords: FlatSB_SetScrollInfo, FlatSB_SetScrollInfo function [Windows Controls], SB_HORZ, SB_VERT, SIF_ALL, SIF_DISABLENOSCROLL, SIF_PAGE, SIF_POS, SIF_RANGE, _win32_FlatSB_SetScrollInfo, _win32_FlatSB_SetScrollInfo_cpp, commctrl/FlatSB_SetScrollInfo, controls.FlatSB_SetScrollInfo, controls._win32_FlatSB_SetScrollInfo
req.header: commctrl.h
req.include-header: 
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FlatSB_SetScrollInfo
 - commctrl/FlatSB_SetScrollInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - FlatSB_SetScrollInfo
---

# FlatSB_SetScrollInfo function


## -description

Sets the information for a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a> function.

## -parameters

### -param unnamedParam1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that contains the flat scroll bar. This window handle must have been passed previously in a call to <a href="/windows/desktop/api/commctrl/nf-commctrl-initializeflatsb">InitializeFlatSB</a>.

### -param code

Type: <b>int</b>

The scroll bar type. It can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Sets the information for the horizontal scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Sets the information for the vertical scroll bar. 

</td>
</tr>
</table>

### -param psi

Type: <b>LPSCROLLINFO</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-scrollinfo">SCROLLINFO</a> structure that contains the new information for the specified scroll bar. The <b>cbSize</b> and 
					<b>fMask</b> members of the structure must be filled in prior to calling <b>FlatSB_SetScrollInfo</b>. The <b>fMask</b> member specifies which members of the structure contain valid information and can be any combination of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SIF_DISABLENOSCROLL"></a><a id="sif_disablenoscroll"></a><dl>
<dt><b>SIF_DISABLENOSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Disables the scroll bar if the new information would cause the scroll bar to be removed. 

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_PAGE"></a><a id="sif_page"></a><dl>
<dt><b>SIF_PAGE</b></dt>
</dl>
</td>
<td width="60%">
Sets the page information for the flat scroll bar. The 
						<b>nPage</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-scrollinfo">SCROLLINFO</a> structure must contain the new page value. 

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_POS"></a><a id="sif_pos"></a><dl>
<dt><b>SIF_POS</b></dt>
</dl>
</td>
<td width="60%">
Sets the position information for the flat scroll bar. The 
						<b>nPos</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-scrollinfo">SCROLLINFO</a> structure must contain the new position value. 

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_RANGE"></a><a id="sif_range"></a><dl>
<dt><b>SIF_RANGE</b></dt>
</dl>
</td>
<td width="60%">
Sets the range information for the flat scroll bar. The 
						<b>nMin</b> and 
						<b>nMax</b> members of the <a href="/windows/desktop/api/winuser/ns-winuser-scrollinfo">SCROLLINFO</a> structure must contain the new range values.

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_ALL"></a><a id="sif_all"></a><dl>
<dt><b>SIF_ALL</b></dt>
</dl>
</td>
<td width="60%">
A combination of SIF_PAGE, SIF_POS, and SIF_RANGE.

</td>
</tr>
</table>

### -param fRedraw

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether the scroll bar should be redrawn immediately to reflect the change. If this parameter is <b>TRUE</b>, the scroll bar is redrawn; if it is <b>FALSE</b>, the scroll bar is not redrawn.

## -returns

Type: <b>int</b>

Returns the current scroll position. If the call to <b>FlatSB_SetScrollInfo</b> changes the scroll position, then the previous position is returned.

## -remarks

<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>