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

# IFolderView2::GetVisibleItem


## -description


Gets the next visible item in relation to a given index in the view.


## -parameters




### -param iStart [in]

Type: <b>int</b>

The zero-based position at which to start searching for a visible item.


### -param fPrevious [in]

Type: <b>BOOL</b>

<b>TRUE</b> to find the first visible item before <i>iStart</i>. <b>FALSE</b> to find the first visible item after <i>iStart</i>.


### -param piItem [out]

Type: <b>int*</b>

When this method returns, contains a pointer to a value that receives the index of the visible item in the view.


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Item retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Item not found. Note that this is a success code.

</td>
</tr>
</table>
 



