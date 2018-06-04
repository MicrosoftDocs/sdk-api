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

# ListView_Arrange macro


## -description


Arranges items in icon view. You can use this macro or send the <a href="https://msdn.microsoft.com/f7dbcdd2-3cc9-4bae-827e-8bac3b49486c">LVM_ARRANGE</a> message explicitly.


## -parameters




### -param hwndLV

TBD


### -param code

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

One of the following values that specifies alignment:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVA_ALIGNLEFT"></a><a id="lva_alignleft"></a><dl>
<dt><b>LVA_ALIGNLEFT</b></dt>
</dl>
</td>
<td width="60%">
Not implemented. Apply the <a href="List_view_window_styles.htm">LVS_ALIGNLEFT</a> style instead.

</td>
</tr>
<tr>
<td width="40%"><a id="LVA_ALIGNTOP"></a><a id="lva_aligntop"></a><dl>
<dt><b>LVA_ALIGNTOP</b></dt>
</dl>
</td>
<td width="60%">
Not implemented. Apply the <a href="List_view_window_styles.htm">LVS_ALIGNTOP</a> style instead.

</td>
</tr>
<tr>
<td width="40%"><a id="LVA_DEFAULT"></a><a id="lva_default"></a><dl>
<dt><b>LVA_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Aligns items according to the list-view control's current alignment styles (the default value).

</td>
</tr>
<tr>
<td width="40%"><a id="LVA_SNAPTOGRID"></a><a id="lva_snaptogrid"></a><dl>
<dt><b>LVA_SNAPTOGRID</b></dt>
</dl>
</td>
<td width="60%">
Snaps all icons to the nearest grid position.

</td>
</tr>
</table>
 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.

