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

# ITextHost::TxEnableScrollBar


## -description


Enables or disables one or both scroll bar arrows in the text host window.


## -parameters




### -param fuSBFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Specifies which scroll bar is affected. This parameter can be one of the following values.

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
Affects both the horizontal and vertical scroll bars.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Affects the horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Affects the vertical scroll bar.

</td>
</tr>
</table>
 


### -param fuArrowflags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Specifies which scroll bar arrows are enabled or disabled. This parameter can be one of the following values.

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
Disables both arrows on a scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_DOWN"></a><a id="esb_disable_down"></a><dl>
<dt><b>ESB_DISABLE_DOWN</b></dt>
</dl>
</td>
<td width="60%">
Disables the down arrow on a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_LEFT"></a><a id="esb_disable_left"></a><dl>
<dt><b>ESB_DISABLE_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Disables the left arrow on a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_LTUP"></a><a id="esb_disable_ltup"></a><dl>
<dt><b>ESB_DISABLE_LTUP</b></dt>
</dl>
</td>
<td width="60%">
Disables the left arrow on a horizontal scroll bar or the up arrow of a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_RIGHT"></a><a id="esb_disable_right"></a><dl>
<dt><b>ESB_DISABLE_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Disables the right arrow on a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_RTDN"></a><a id="esb_disable_rtdn"></a><dl>
<dt><b>ESB_DISABLE_RTDN</b></dt>
</dl>
</td>
<td width="60%">
Disables the right arrow on a horizontal scroll bar or the down arrow of a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_UP"></a><a id="esb_disable_up"></a><dl>
<dt><b>ESB_DISABLE_UP</b></dt>
</dl>
</td>
<td width="60%">
Disables the up arrow on a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_ENABLE_BOTH"></a><a id="esb_enable_both"></a><dl>
<dt><b>ESB_ENABLE_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Enables both arrows on a scroll bar.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Return nonzero if the arrows are enabled or disabled as specified. 

Return zero if the arrows are already in the requested state or an error occurs.




## -remarks



This method is only valid when the control is in-place active; calls while the control is inactive may fail.




## -see-also




<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls Overview</a>
 

 

