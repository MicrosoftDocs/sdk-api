---
UID: NF:commctrl.FlatSB_ShowScrollBar
title: FlatSB_ShowScrollBar function
author: windows-driver-content
description: Shows or hides a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard ShowScrollBar function.
old-location: controls\FlatSB_ShowScrollBar.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\flatsb_showscrollbar.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: FlatSB_ShowScrollBar, FlatSB_ShowScrollBar function [Windows Controls], SB_BOTH, SB_HORZ, SB_VERT, _win32_FlatSB_ShowScrollBar, _win32_FlatSB_ShowScrollBar_cpp, commctrl/FlatSB_ShowScrollBar, controls.FlatSB_ShowScrollBar, controls._win32_FlatSB_ShowScrollBar
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comctl32.dll
api_name:
-	FlatSB_ShowScrollBar
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 4.71 or later)
req.irql: 
---

# FlatSB_ShowScrollBar function


## -description


Shows or hides a flat scroll bar. If flat scroll bars are not initialized for the window, this function calls the standard <a href="https://msdn.microsoft.com/a3c66874-b2a8-485a-9b03-bc28db74ca6c">ShowScrollBar</a> function. 


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
<td width="40%"><a id="SB_BOTH"></a><a id="sb_both"></a><dl>
<dt><b>SB_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Shows or hides the horizontal and vertical scroll bars. 

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Shows or hides the horizontal scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Shows or hides the vertical scroll bar. 

</td>
</tr>
</table>
 


#### - fShow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether the scroll bar should be shown or hidden. If this parameter is nonzero, the scroll bar will be shown; if it is zero, the scroll bar will be hidden. 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window that contains the flat scroll bar. This window handle must have been passed previously in a call to <a href="https://msdn.microsoft.com/ecad7e1b-5250-47fc-bc0f-81889186729f">InitializeFlatSB</a>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 




## -remarks



<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>


