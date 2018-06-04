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

# IServiceActivity::AsynchronousCall


## -description


Performs the user-defined work asynchronously.


## -parameters




### -param pIServiceCall [in]

A pointer to the <a href="https://msdn.microsoft.com/97532e29-3d1a-4a7c-8103-dd7ae2866a70">IServiceCall</a> interface that is used to implement the batch work.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_FAIL, as well as the following values.

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
The batch work was accepted by the activity to run asynchronously. This return value does not necessarily mean that the batch work successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_ASYNC_WORK_REJECTED</b></dt>
</dl>
</td>
<td width="60%">
The batch work cannot be added to the asynchronous work queue of the activity.


</td>
</tr>
</table>
 




## -remarks



The batch work that is run by this method runs in the context and thread apartment of the activity that was created by the call to <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>.





## -see-also




<a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a>
 

 

