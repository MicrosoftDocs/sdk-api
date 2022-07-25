---
UID: NF:commctrl.FlatSB_GetScrollPos
title: FlatSB_GetScrollPos function (commctrl.h)
description: Gets the thumb position in a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard GetScrollPos function.
helpviewer_keywords: ["FlatSB_GetScrollPos","FlatSB_GetScrollPos function [Windows Controls]","SB_HORZ","SB_VERT","_win32_FlatSB_GetScrollPos","_win32_FlatSB_GetScrollPos_cpp","commctrl/FlatSB_GetScrollPos","controls.FlatSB_GetScrollPos","controls._win32_FlatSB_GetScrollPos"]
old-location: controls\FlatSB_GetScrollPos.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\flatsb_getscrollpos.htm
ms.date: 12/05/2018
ms.keywords: FlatSB_GetScrollPos, FlatSB_GetScrollPos function [Windows Controls], SB_HORZ, SB_VERT, _win32_FlatSB_GetScrollPos, _win32_FlatSB_GetScrollPos_cpp, commctrl/FlatSB_GetScrollPos, controls.FlatSB_GetScrollPos, controls._win32_FlatSB_GetScrollPos
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
 - FlatSB_GetScrollPos
 - commctrl/FlatSB_GetScrollPos
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
 - FlatSB_GetScrollPos
---

# FlatSB_GetScrollPos function


## -description

Gets the thumb position in a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/winuser/nf-winuser-getscrollpos">GetScrollPos</a> function.

## -parameters

### -param unnamedParam1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that contains the flat scroll bar. This window handle must have been passed previously in a call to <a href="/windows/desktop/api/commctrl/nf-commctrl-initializeflatsb">InitializeFlatSB</a>.

### -param code

Type: <b>int</b>

The parameter that specifies the scroll bar type. It can be one of the following values: 

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
Retrieves the thumb position of the horizontal scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the thumb position of the vertical scroll bar. 

</td>
</tr>
</table>

## -returns

Type: <b>int</b>

Returns the current thumb position of the specified flat scroll bar.

## -remarks

<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>