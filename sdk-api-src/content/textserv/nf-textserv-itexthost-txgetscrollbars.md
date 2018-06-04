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

# ITextHost::TxGetScrollBars


## -description


Requests information about the scroll bars supported by the text host.


## -parameters




### -param pdwScrollBar

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The scroll bar. This parameter can be a combination of the following window styles related to scroll bars. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WS_VSCROLL"></a><a id="ws_vscroll"></a><dl>
<dt><b>WS_VSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Supports a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WS_HSCROLL"></a><a id="ws_hscroll"></a><dl>
<dt><b>WS_HSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Supports a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_AUTOVSCROLL"></a><a id="es_autovscroll"></a><dl>
<dt><b>ES_AUTOVSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Automatically scrolls text up one page when the user presses ENTER on the last line.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_AUTOHSCROLL"></a><a id="es_autohscroll"></a><dl>
<dt><b>ES_AUTOHSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Automatically scrolls text to the right by 10 characters when the user types a character at the end of the line. When the user presses ENTER, the control scrolls all text back to position zero.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_DISABLENOSCROLL"></a><a id="es_disablenoscroll"></a><dl>
<dt><b>ES_DISABLENOSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Disables scroll bars instead of hiding them when they are not needed.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

The return value is <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls Overview</a>
 

 

