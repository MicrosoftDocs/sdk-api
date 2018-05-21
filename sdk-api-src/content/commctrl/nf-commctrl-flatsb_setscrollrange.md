---
UID: NF:commctrl.FlatSB_SetScrollRange
title: FlatSB_SetScrollRange function
author: windows-driver-content
description: Sets the scroll range of a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard SetScrollRange function.
old-location: controls\FlatSB_SetScrollRange.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\flatsb_setscrollrange.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: FlatSB_SetScrollRange, FlatSB_SetScrollRange function [Windows Controls], SB_HORZ, SB_VERT, _win32_FlatSB_SetScrollRange, _win32_FlatSB_SetScrollRange_cpp, commctrl/FlatSB_SetScrollRange, controls.FlatSB_SetScrollRange, controls._win32_FlatSB_SetScrollRange
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comctl32.dll
api_name:
-	FlatSB_SetScrollRange
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 4.71 or later)
req.irql: 
---

# FlatSB_SetScrollRange function


## -description


Sets the scroll range of a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard <a href="https://msdn.microsoft.com/749c3b04-d5a6-4f7c-89a3-a1c0fbb85cb9">SetScrollRange</a> function. 


## -parameters




### -param param

TBD


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
Sets the scroll range of the horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Sets the scroll range of the vertical scroll bar. 

</td>
</tr>
</table>
 


### -param min

TBD


### -param max

TBD


### -param fRedraw

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether the scroll bar should be redrawn immediately to reflect the change. If this parameter is <b>TRUE</b>, the scroll bar is redrawn; if it is <b>FALSE</b>, the scroll bar is not redrawn. 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window that contains the flat scroll bar. This window handle must have been passed previously in a call to <a href="https://msdn.microsoft.com/ecad7e1b-5250-47fc-bc0f-81889186729f">InitializeFlatSB</a>. 


#### - nMaxPos

Type: <b>int</b>

The new maximum scroll range value. 


#### - nMinPos

Type: <b>int</b>

The new minimum scroll range value. 


## -returns



Type: <b>int</b>

Returns nonzero if successful, or zero otherwise. 




## -remarks



<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>


