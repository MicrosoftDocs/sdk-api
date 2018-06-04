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

# IKnowledgeSyncProvider::GetChangeBatch


## -description


Gets a change batch that contains item metadata for items that are not contained in the specified knowledge from the destination provider.


## -parameters




### -param dwBatchSize [in]

The requested number of changes to include in the change batch.


### -param pSyncKnowledge [in]

The knowledge from the destination provider. This knowledge must be mapped by calling  <a href="https://msdn.microsoft.com/9325ff3e-4f8e-4a18-bc95-57af30ccd437">ISyncKnowledge::MapRemoteToLocal</a> on the source knowledge before it can be used for change enumeration.


### -param ppSyncChangeBatch [out]

Returns a change batch that contains item metadata for items that are not contained in <i>pSyncKnowledge</i>.


### -param ppUnkDataRetriever [out]

Returns an object that can be used to retrieve change data. It can be an <a href="https://msdn.microsoft.com/d59a5198-5878-4a48-b6c4-042afc36054d">ISynchronousDataRetriever</a> object or a provider-specific object.


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



Be aware that <i>dwBatchSize</i> is a requested number only. A smaller or larger batch can be returned.


<div class="alert"><b>Note</b>  If there are no more changes to send after this batch, <a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase::SetLastBatch</a> must be called on the returned change batch before <b>GetChangeBatch</b> is called again.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/396bbf7e-7fd0-4a2e-8304-f87097cd5e50">IKnowledgeSyncProvider Interface</a>
 

 

