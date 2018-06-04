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

# ISyncChangeBatchAdvanced::GetBatchLevelKnowledgeShouldBeApplied


## -description


Gets a value that indicates whether the learned knowledge for the batch must be saved after the batch is applied to the destination replica.


## -parameters




### -param pfBatchKnowledgeShouldBeApplied [out]

Returns a value that indicates whether the learned knowledge for the batch must be saved after the batch is applied to the destination replica.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_BATCH_NEEDS_KNOWLEDGE</b></dt>
</dl>
</td>
<td width="60%">
The change batch contains no changes and no knowledge.

</td>
</tr>
</table>
 




## -remarks



Typically, the destination provider saves the learned knowledge for each item change as it is applied to the destination replica. The value that is returned by <b>GetBatchLevelKnowledgeShouldBeApplied</b> indicates whether it is also necessary to save the learned knowledge of the change batch after the entire change batch has been applied. The learned knowledge of the change batch can be obtained by calling <a href="https://msdn.microsoft.com/cef04646-71a7-489d-9beb-fe87bb949218">ISyncChangeBatchBase::GetLearnedKnowledge</a>.




## -see-also




<a href="https://msdn.microsoft.com/b78bc885-ed4e-4c83-ad1b-043c5b226337">ISyncChangeBatchAdvanced Interface</a>



<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>
 

 

