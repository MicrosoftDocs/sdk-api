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

# ISyncSessionState::OnProgress


## -description


Reports synchronization progress to the application.


## -parameters




### -param provider [in]

The role of the provider that is sending this event.


### -param syncStage [in]

The current stage of the synchronization session.


### -param dwCompletedWork [in]

The amount of work that is currently completed in the session. This value is interpreted as being a part of <i>dwTotalWork</i>.


### -param dwTotalWork [in]

The total work for the session.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>provider</i> or <i>syncStage</i> is not a valid value.

</td>
</tr>
</table>
 




## -remarks



This method can be used to report custom progress to the application. When a provider calls this method, the <a href="https://msdn.microsoft.com/4a4dad07-b169-4767-a118-3b5c6c8b9764">ISyncCallback::OnProgress</a> event is raised.




## -see-also




<a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback Interface</a>



<a href="https://msdn.microsoft.com/9b03d5af-b5f5-49fa-a10e-9f9f3c1dab0e">ISyncSessionState Interface</a>



<a href="https://msdn.microsoft.com/06f8542a-d742-4cbb-bb44-c107b59ad38f">SYNC_PROGRESS STAGE Enumeration</a>



<a href="https://msdn.microsoft.com/2409c8bf-c4fc-4986-8dde-cc11f0d52ed4">SYNC_PROVIDER ROLE Enumeration</a>
 

 

