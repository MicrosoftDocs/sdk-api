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

# ListView_GetItemState macro


## -description


Gets the state of a list-view item. You can use this macro or send the <a href="https://msdn.microsoft.com/862960ed-a64a-4d66-b384-9228932eae6f">LVM_GETITEMSTATE</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param i

Type: <b>int</b>

The index of the list-view item. 


### -param mask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The state information to retrieve. This parameter can be a combination of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVIS_CUT"></a><a id="lvis_cut"></a><dl>
<dt><b>LVIS_CUT</b></dt>
</dl>
</td>
<td width="60%">
The item is marked for a cut-and-paste operation.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_DROPHILITED"></a><a id="lvis_drophilited"></a><dl>
<dt><b>LVIS_DROPHILITED</b></dt>
</dl>
</td>
<td width="60%">
The item is highlighted as a drag-and-drop target.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_FOCUSED"></a><a id="lvis_focused"></a><dl>
<dt><b>LVIS_FOCUSED</b></dt>
</dl>
</td>
<td width="60%">
The item has the focus, so it is surrounded by a standard focus rectangle. Although more than one item may be selected, only one item can have the focus.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_SELECTED"></a><a id="lvis_selected"></a><dl>
<dt><b>LVIS_SELECTED</b></dt>
</dl>
</td>
<td width="60%">
The item is selected. The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_OVERLAYMASK"></a><a id="lvis_overlaymask"></a><dl>
<dt><b>LVIS_OVERLAYMASK</b></dt>
</dl>
</td>
<td width="60%">
Use this mask to retrieve the item's overlay image index.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_STATEIMAGEMASK"></a><a id="lvis_stateimagemask"></a><dl>
<dt><b>LVIS_STATEIMAGEMASK</b></dt>
</dl>
</td>
<td width="60%">
Use this mask to retrieve the item's state image index.

</td>
</tr>
</table>
 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



An item's state information includes a set of bit flags as well as image list indexes that indicate the item's state image and overlay image. 




## -see-also




<a href="https://msdn.microsoft.com/b90900f1-833b-418c-8ddc-76c0743b77f9">ListView_SetItemState</a>
 

 

