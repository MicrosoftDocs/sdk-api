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

# ITACDGroupEvent::get_Event


## -description


The 
<b>get_Event</b> method gets the descriptor of an event which indicates that a new ACD group has been added.


## -parameters




### -param pEvent [out]

Pointer to 
<a href="https://msdn.microsoft.com/fb3de7e5-5a29-4f7b-8b2a-252536dedae6">ACDGROUP_EVENT</a> descriptor of event.


## -returns



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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



The ACDGE_NEW_GROUP and ACDGE_REMOVE_GROUP values are not currently supported.




## -see-also




<a href="https://msdn.microsoft.com/fb3de7e5-5a29-4f7b-8b2a-252536dedae6">ACDGROUP_EVENT</a>



<a href="https://msdn.microsoft.com/5770dca5-cf71-4211-ba9f-0fe7a3bbb614">ITACDGroupEvent</a>
 

 

