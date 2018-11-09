---
UID: NF:commctrl.FlatSB_SetScrollPos
title: FlatSB_SetScrollPos function
author: windows-sdk-content
description: Sets the current position of the thumb in a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard SetScrollPos function.
old-location: controls\FlatSB_SetScrollPos.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\flatsb_setscrollpos.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FlatSB_SetScrollPos, FlatSB_SetScrollPos function [Windows Controls], SB_HORZ, SB_VERT, _win32_FlatSB_SetScrollPos, _win32_FlatSB_SetScrollPos_cpp, commctrl/FlatSB_SetScrollPos, controls.FlatSB_SetScrollPos, controls._win32_FlatSB_SetScrollPos
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - FlatSB_SetScrollPos
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FlatSB_SetScrollPos function


## -description


Sets the current position of the thumb in a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard <a href="https://msdn.microsoft.com/en-us/library/Bb787597(v=VS.85).aspx">SetScrollPos</a> function. 


## -parameters




### -param arg1

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the window that contains the flat scroll bar. This window handle must have been passed previously in a call to <a href="https://msdn.microsoft.com/en-us/library/Bb775443(v=VS.85).aspx">InitializeFlatSB</a>. 


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
Sets the thumb position of the horizontal scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Sets the thumb position of the vertical scroll bar. 

</td>
</tr>
</table>
 


### -param pos

Type: <b>int</b>

The new thumb position. 


### -param fRedraw

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Specifies whether the scroll bar should be redrawn immediately to reflect the change. If this parameter is <b>TRUE</b>, the scroll bar is redrawn; if it is <b>FALSE</b>, the scroll bar is not redrawn. 


## -returns



Type: <b>int</b>

Returns the previous position of the thumb in the specified flat scroll bar. 




## -remarks



<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>


