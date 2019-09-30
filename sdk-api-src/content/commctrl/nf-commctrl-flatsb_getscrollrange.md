---
UID: NF:commctrl.FlatSB_GetScrollRange
title: FlatSB_GetScrollRange function (commctrl.h)
author: windows-sdk-content
description: Gets the scroll range for a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard GetScrollRange function.
old-location: controls\FlatSB_GetScrollRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\flatsb_getscrollrange.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FlatSB_GetScrollRange, FlatSB_GetScrollRange function [Windows Controls], SB_HORZ, SB_VERT, _win32_FlatSB_GetScrollRange, _win32_FlatSB_GetScrollRange_cpp, commctrl/FlatSB_GetScrollRange, controls.FlatSB_GetScrollRange, controls._win32_FlatSB_GetScrollRange
ms.topic: function
f1_keywords: 
 - "commctrl/FlatSB_GetScrollRange"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - FlatSB_GetScrollRange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FlatSB_GetScrollRange function


## -description


Gets the scroll range for a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getscrollrange">GetScrollRange</a> function. 


## -parameters




### -param arg1

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that contains the flat scroll bar. This window handle must have been passed previously in a call to <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-initializeflatsb">InitializeFlatSB</a>. 


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
Retrieves the scroll range of the horizontal scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the scroll range of the vertical scroll bar. 

</td>
</tr>
</table>
 


### -param arg3

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPINT</a></b>

A pointer to an INT value that receives the minimum scroll range value. 


### -param arg4

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPINT</a></b>

A pointer to an INT value that receives the maximum scroll range value. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.




## -remarks



<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>


