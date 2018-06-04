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

# ISyncMgrSynchronize::GetItemObject


## -description


Obtains an interface on a specified item that a registered application handles.


## -parameters




### -param ItemID [in]

Type: <b>REFGUID</b>

An identifier for a requested item.


### -param riid [in]

Type: <b>REFIID</b>

An identifier for a requested interface.


### -param ppv [out]

Type: <b>void**</b>

An address of a variable that receives a pointer to a requested interface.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The requested interface is not found.

</td>
</tr>
</table>
 




## -remarks



This method exists only for forward compatibility. Currently, there are no interfaces defined on an item. Application implementers must return E_NOTIMPL from this method.




## -see-also




<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>
 

 

