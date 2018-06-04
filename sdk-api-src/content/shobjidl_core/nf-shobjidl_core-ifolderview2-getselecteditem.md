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

# IFolderView2::GetSelectedItem


## -description


Locates the currently selected item at or after a given index.


## -parameters




### -param iStart [in]

Type: <b>int</b>

The index position from which to start searching for the currently selected item.


### -param piItem [out]

Type: <b>int*</b>

A pointer to a value that receives the index of the item in the view.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if a selected item was found, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Item not found. Note that this is a success code. The operation was successful in searching the view, it simply did not find a currently selected item after the given index (<i>iStart</i>). It is possible that no item was selected, or that the selected item had an index less than <i>iStart</i>.

</td>
</tr>
</table>
 



