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

# IKnowledgeSyncProvider::EndSession


## -description


Notifies the provider that a synchronization session to which it was enlisted has finished.


## -parameters




### -param pSessionState [in]

The current status of the corresponding session.


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
<dt><b>Provider-determined error codes</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



<i>pSessionState</i> will be equal to the <b>ISyncSessionState</b> object that was provided to the previous corresponding call to <a href="https://msdn.microsoft.com/15aae98e-96c6-45f3-906f-1729fa79ebdb">IKnowledgeSyncProvider::BeginSession</a>.

<div class="alert"><b>Note</b>  This method must return an error, typically <a href="https://msdn.microsoft.com/da86cf89-885b-42bc-9fcb-0c9114a36f78">SYNC_E_INVALIDOPERATION</a>, if the provider did not receive a previous call to <a href="https://msdn.microsoft.com/15aae98e-96c6-45f3-906f-1729fa79ebdb">BeginSession</a> for the specified session.

<p class="note">When this method is called, the provider must release any references it has to the <b>ISyncSessionState</b> object that is specified by <i>pSessionState</i>.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/396bbf7e-7fd0-4a2e-8304-f87097cd5e50">IKnowledgeSyncProvider Interface</a>
 

 

