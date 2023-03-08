---
UID: NF:commctrl.FlatSB_EnableScrollBar
title: FlatSB_EnableScrollBar function (commctrl.h)
description: Enables or disables one or both flat scroll bar direction buttons. If flat scroll bars are not initialized for the window, this function calls the standard EnableScrollBar function.
helpviewer_keywords: ["ESB_DISABLE_BOTH","ESB_DISABLE_DOWN","ESB_DISABLE_LEFT","ESB_DISABLE_LTUP","ESB_DISABLE_RIGHT","ESB_DISABLE_RTDN","ESB_DISABLE_UP","ESB_ENABLE_BOTH","FlatSB_EnableScrollBar","FlatSB_EnableScrollBar function [Windows Controls]","SB_BOTH","SB_HORZ","SB_VERT","_win32_FlatSB_EnableScrollBar","_win32_FlatSB_EnableScrollBar_cpp","commctrl/FlatSB_EnableScrollBar","controls.FlatSB_EnableScrollBar","controls._win32_FlatSB_EnableScrollBar"]
old-location: controls\FlatSB_EnableScrollBar.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\flatsb_enablescrollbar.htm
ms.date: 12/05/2018
ms.keywords: ESB_DISABLE_BOTH, ESB_DISABLE_DOWN, ESB_DISABLE_LEFT, ESB_DISABLE_LTUP, ESB_DISABLE_RIGHT, ESB_DISABLE_RTDN, ESB_DISABLE_UP, ESB_ENABLE_BOTH, FlatSB_EnableScrollBar, FlatSB_EnableScrollBar function [Windows Controls], SB_BOTH, SB_HORZ, SB_VERT, _win32_FlatSB_EnableScrollBar, _win32_FlatSB_EnableScrollBar_cpp, commctrl/FlatSB_EnableScrollBar, controls.FlatSB_EnableScrollBar, controls._win32_FlatSB_EnableScrollBar
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
 - FlatSB_EnableScrollBar
 - commctrl/FlatSB_EnableScrollBar
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
 - FlatSB_EnableScrollBar
---

# FlatSB_EnableScrollBar function


## -description

Enables or disables one or both flat scroll bar direction buttons. If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/winuser/nf-winuser-enablescrollbar">EnableScrollBar</a> function.

## -parameters

### -param unnamedParam1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that contains the flat scroll bar. This window handle must have been passed previously in a call to <a href="/windows/desktop/api/commctrl/nf-commctrl-initializeflatsb">InitializeFlatSB</a>.

### -param unnamedParam2

Type: <b>int</b>

A parameter that specifies the scroll bar type. It can be one of the following values: 

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
Enables or disables the direction buttons on the horizontal and vertical scroll bars.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Enables or disables the direction buttons on the horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Enables or disables the direction buttons on the vertical scroll bar. 

</td>
</tr>
</table>

### -param unnamedParam3

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A parameter that specifies whether the scroll bar arrows are enabled or disabled and indicates which arrows are enabled or disabled. It can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_BOTH"></a><a id="esb_disable_both"></a><dl>
<dt><b>ESB_DISABLE_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Disables both direction buttons on the specified scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_DOWN"></a><a id="esb_disable_down"></a><dl>
<dt><b>ESB_DISABLE_DOWN</b></dt>
</dl>
</td>
<td width="60%">
Disables the down direction button on the vertical scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_LEFT"></a><a id="esb_disable_left"></a><dl>
<dt><b>ESB_DISABLE_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Disables the left direction button on the horizontal scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_LTUP"></a><a id="esb_disable_ltup"></a><dl>
<dt><b>ESB_DISABLE_LTUP</b></dt>
</dl>
</td>
<td width="60%">
Disables the left direction button on the horizontal scroll bar or the up direction button on the vertical scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_RIGHT"></a><a id="esb_disable_right"></a><dl>
<dt><b>ESB_DISABLE_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Disables the right direction button on the horizontal scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_RTDN"></a><a id="esb_disable_rtdn"></a><dl>
<dt><b>ESB_DISABLE_RTDN</b></dt>
</dl>
</td>
<td width="60%">
Disables the right direction button on the horizontal scroll bar or the down direction button on the vertical scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_UP"></a><a id="esb_disable_up"></a><dl>
<dt><b>ESB_DISABLE_UP</b></dt>
</dl>
</td>
<td width="60%">
Disables the up direction button on the vertical scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_ENABLE_BOTH"></a><a id="esb_enable_both"></a><dl>
<dt><b>ESB_ENABLE_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Enables both direction buttons on the specified scroll bar. 

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if the scroll bar changes, or zero otherwise.

## -remarks

<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>