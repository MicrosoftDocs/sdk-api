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

# ISyncChangeBatchBase::GetIsLastBatch


## -description


Gets a flag that indicates whether the changes in this change batch are the last batch of a synchronization session.


## -parameters




### -param pfLastBatch [out]

Returns a flag that indicates whether this batch is the last batch.


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
<dt><b>E_POINTER

</b></dt>
</dl>
</td>
<td width="60%">
<i>pfLastBatch</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



When returning a change batch in response to the <a href="https://msdn.microsoft.com/165eb8eb-092c-4084-a296-abc2421596d5">IKnowledgeSyncProvider::GetChangeBatch</a> method, the source provider must call <a href="https://msdn.microsoft.com/7619b446-5c71-4533-8af6-15f06dda3c87">SetLastBatch</a> if the change batch is the last batch of changes. 




## -see-also




<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>
 

 

