---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# FlatSB_EnableScrollBar function


## -description


Enables or disables one or both flat scroll bar direction buttons. If flat scroll bars are not initialized for the window, this function calls the standard <a href="https://msdn.microsoft.com/f00224d5-5f37-4b18-91e2-63c66797b243">EnableScrollBar</a> function. 


## -parameters




### -param

TBD




#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window that contains the flat scroll bar. This window handle must have been passed previously in a call to <a href="https://msdn.microsoft.com/ecad7e1b-5250-47fc-bc0f-81889186729f">InitializeFlatSB</a>. 


#### - wArrows

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

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
 


#### - wSBflags

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
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if the scroll bar changes, or zero otherwise. 




## -remarks



<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>


